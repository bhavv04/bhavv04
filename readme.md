```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

typedef struct {
    char name[32];
    char stack[128];
    char learning[64];
    int commits_today;
} developer_t;

void init_developer(developer_t *dev) {
    strcpy(dev->name, "Bhavdeep Arora");
    strcpy(dev->stack, "C, Rust, Assembly, Python");
    strcpy(dev->learning, "Kernel Development");
    dev->commits_today = 5;
}

void ship_code(developer_t *dev) {
    printf("Shipping from %p\n", (void*)dev);
    dev->commits_today++;
}

int main() {
    developer_t me;
    init_developer(&me);
    
    while (1) {
        ship_code(&me);
    }
    
    return 0; // never reached
}
```
