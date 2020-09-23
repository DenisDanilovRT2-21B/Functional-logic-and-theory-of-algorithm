#include <stdio.h>
#include <stdlib.h>
struct turn {
    int arr[11];
    int first;
    int last;
};
int y;
int element;
void initial(struct turn *p ) {
    p->first = 1;
    p->last = 0;
}
void put_into(struct turn *p) {
    y = 0;
    if (p->last < 10) {
        printf("Введите элемент:");
        scanf("%d",&element);
        p->last++;
        p->arr[p->last] = element;
    }
  else {
      printf("Очередь переполнена\n");
  }
}

int check_empty(struct turn *p) {
 if(p->first > p->last) {
    y = 1;
    return y;
 }
  else {
       y = 0;
       return y;
  }
}

int put_out(struct turn *p) {
    check_empty(p);
    int x,i;
    if (y == 1) {
       printf("Очередь пуста\n");
       return 0;
}
    else {
        x = p->arr[p->first];
        for (i = p->first; i < p->last;i++) {
         p->arr[x] = p->arr[x + 1];
        }
      p->last--;
      return x;
    }
}

int show(struct turn *p) {
check_empty(p);
    if (y == 1) {
    printf("Очередь пуста\n");
    return 0;
    }
    else {
        int i;
        for(i = p->first; i <= p->last;i++) {
            printf("%d ",p->arr[i]);
        }
    return 0;
    }
}

int main(void) {
    int start;
    setlocale(0,"");
    struct turn *p;
    p = malloc(sizeof(struct turn));
    initial(p);
    check_empty(p);
    printf("Задание \"Очередь\"\n");
    printf("Для начала работы нажмите одну из соответствующих цифр:\n");
    printf("1.Вывести все элементы очереди\n");
    printf("2.Добавить элемент\n");
    printf("3.Удалить элемент\n");
    printf("4.Завершить работу\n");
    while (1) {
        scanf("%d",&start);
        switch(start) {
            case 1:
            show(p);
            printf("\n\n");
            break;
            case 2:
            put_into(p);
            printf("\n");
            break;
            case 3:
            put_out(p);
            printf("\n");
            break;
            case 4:
            printf("\n");
            return 0;
            break;
            default:
            printf("Ошибка.Повторите.\n\n");
        }
   }
}
