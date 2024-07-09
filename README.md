#include <stdio.h>
#include <math.h>

int main() {
    double x1, y1, r1, x2, y2, r2;
    double distance;

    scanf("%lf %lf %lf %lf %lf %lf", &x1, &y1, &r1, &x2, &y2, &r2);

    distance = sqrt((x2 - x1) * (x2 - x1) + (y2 - y1) * (y2 - y1));

    if (distance == 0 && r1 == r2) {

        printf("-1\n");
    } else if (distance > r1 + r2 || distance < fabs(r1 - r2)) {

        printf("0\n");
    } else if (distance == r1 + r2 || distance == fabs(r1 - r2)) {

        printf("1\n");
    } else {

        printf("2\n");
    }

    return 0;
}