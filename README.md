# A-Mazeing-Dungeon
> Console based game inspired by the Dungeon Maze game.


## General info
Group project exercise 

## Screenshots
![](dragon.png)
![](map.png)

## Technologies
* Java 11

## Setup
Import to optional IDE.

## Code Examples
` public void heroFight(Monster monster) throws InterruptedException {

        boolean control = true;
        monster.displayInfo();

        while (control) {

            int fight = attack();
            int fightMonster = attackMonster();


            if (fight >= 50) {
                int changeMonsterHealth = monster.getHealth();
                System.out.println(" ");
                System.out.println("You hit the enemy!");
                int newMonsterHealth = monster.setMonsterHealth(changeMonsterHealth - this.totalDamage);

                if (newMonsterHealth <= 0) {
                    System.out.println("Enemy died.");
                    levelUp();
                    control = false;
                } else {
                    System.out.println("Enemy health: " + monster.setMonsterHealth(changeMonsterHealth - this.totalDamage) + "/" + monster.maxHealth);
                    Thread.sleep(1500);
                }

            } else {
                System.out.println(" ");
                System.out.println("You missed!");
            }

            if (monster.getHealth() > 0) {
                if (fightMonster >= 50) {
                    int changeHeroHealth = super.getHealth();
                    System.out.println(" ");
                    System.out.println("The enemy hit you!");
                    int newHeroHealth = super.setHeroHealth(changeHeroHealth - monster.getDamage());

                    if (newHeroHealth <= 0) {
                        System.out.println("You died.");
                        //System.out.println("Health: 0" + "/" + super.maxHealth);
                        control = false;
                    } else {
                        System.out.println("Health: " + super.setHeroHealth(changeHeroHealth - monster.getDamage()) + "/" + super.maxHealth);
                        Thread.sleep(1500);
                    }

                } else {
                    System.out.println(" ");
                    System.out.println("Enemy missed!");
                }
            }

        }
    }
`

## Features
* Fight enemy
* Buy weapon
* Find potion
* Move player
* Map
* Save/Load game
* Graphics
* Level up
* Sound

## Status
Project is:_finished_

## Contact
Created by Alex, Chiharu, Mantas, Victor and Patrik - feel free to contact us!
