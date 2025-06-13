```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

typedef struct {
    char name[32];
    char stack[128];
    char learning[64];
    char contact[128];
    int commits_today;
} developer_t;

void init_developer(developer_t *dev) {
    strcpy(dev->name, "Bhavdeep Arora");
    strcpy(dev->stack, "C, Rust, Assembly, Python, Java");
    strcpy(dev->learning, "Kernel Development");
    strcpy(dev->contact, "bhavdeepsa@gmail.com");
}
int main() {
    developer_t me;
    init_developer(&me);
    
    return 0; 
}
```
