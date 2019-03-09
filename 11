#include <stdio.h>

typedef struct { double x, y; } Vec;

int triangle(Vec p, Vec v[3]) {
    int j = 0, i = 2;
    for (; j < 3; i = j++) {
        Vec a = { v[i].y - v[j].y, v[j].x - v[i].x };
        Vec d = { p.x - v[i].x, p.y - v[i].y };
        if (a.x * d.x + a.y * d.y > 0)
            return 0;
    }
    return 1;
}

int main() {
    Vec p, v[] = { { -30, -20 }, { -20, 30 }, { 20, 20 } };
    for (p.y = 40; p.y >= -40; p.y -= 2, putchar('\n'))
        for (p.x = -40; p.x <= 40; p.x++)
             putchar(".*"[triangle(p, v)]);
}
