#include <stdio.h>

#define MAX_SLOTS 10

int main() {

    int shelf[MAX_SLOTS] = {0};   
    int choice, slot;
    int count = 0;
    int i;

    while (1) {
        printf("\n=====================================\n");
        printf("      WAREHOUSE SHELF TRACKER\n");
        printf("=====================================\n");
        printf("1. Add item to a slot\n");
        printf("2. Remove item from a slot\n");
        printf("3. View shelf status\n");
        printf("4. Find first empty slot\n");
        printf("5. Count empty slots\n");
        printf("6. Clear entire shelf\n");
        printf("7. Exit\n");
        printf("=====================================\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);
        printf("=====================================\n");


        if (choice == 1) {
            if (count == MAX_SLOTS) {
                printf("Shelf is FULL! Cannot add more items.\n");
            } else {
                printf("Enter slot number to add (0-9): ");
                scanf("%d", &slot);

                if (slot < 0 || slot >= MAX_SLOTS) {
                    printf("Invalid slot! Choose between 0 and 9.\n");
                } 
                else if (shelf[slot] == 1) {
                    printf("That slot is already occupied!\n");
                } 
                else {
                    shelf[slot] = 1;
                    count++;
                    printf("Item successfully added to slot %d.\n", slot);

                    if (count == MAX_SLOTS) {
                        printf("WARNING: Shelf is now completely full!\n");
                    }
                }
            }
        }

        else if (choice == 2) {
            printf("Enter slot number to remove (0-9): ");
            scanf("%d", &slot);

            if (slot < 0 || slot >= MAX_SLOTS) {
                printf("Invalid slot! Choose between 0 and 9.\n");
            } 
            else if (shelf[slot] == 0) {
                printf("Slot %d is already empty!\n", slot);
            } 
            else {
                shelf[slot] = 0;
                count--;
                printf("Item removed from slot %d.\n", slot);

                if (count == 0) {
                    printf("Shelf is now completely empty.\n");
                }
            }
        }


        else if (choice == 3) {
            printf("Current Shelf Status:\n");
            printf("----------------------------\n");

            for (i = 0; i < MAX_SLOTS; i++) {
                if (shelf[i] == 1)
                    printf("Slot %d : Occupied\n", i);
                else
                    printf("Slot %d : Empty\n", i);
            }

            printf("----------------------------\n");
            printf("Total items stored: %d\n", count);
            printf("Total empty slots: %d\n", MAX_SLOTS - count);

            if (count == MAX_SLOTS)
                printf("SHELF STATUS: FULL\n");
            else if (count == 0)
                printf("SHELF STATUS: EMPTY\n");
            else
                printf("SHELF STATUS: PARTIALLY FILLED\n");
        }


        else if (choice == 4) {
            int found = 0;

            for (i = 0; i < MAX_SLOTS; i++) {
                if (shelf[i] == 0) {
                    printf("First empty slot is: %d\n", i);
                    found = 1;
                    break;
                }
            }

            if (!found)
                printf("No empty slot found. Shelf is full!\n");
        }


        else if (choice == 5) {
            int empty = MAX_SLOTS - count;

            printf("Total empty slots: %d\n", empty);

            if (empty == 0)
                printf("Shelf is completely full.\n");
            else if (empty == MAX_SLOTS)
                printf("Shelf is completely empty.\n");
        }


        else if (choice == 6) {
            for (i = 0; i < MAX_SLOTS; i++)
                shelf[i] = 0;

            count = 0;

            printf("All slots have been cleared.\n");
            printf("Shelf is now completely empty.\n");
        }

        else if (choice == 7) {
            printf("Exiting program... Goodbye!\n");
            break;
        }

        else {
            printf("Invalid choice! Please select a valid option.\n");
        }
    }

    return 0;
}

