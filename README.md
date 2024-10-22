# Welcome to the test for Technical Support Engineer at Climapulse!

## Setup

#### Clone this repository

      $ git clone git@github.com:climapulse/technical-support-test.git

#### Run the Docker setup

    $ docker-compose up --build -d

#### Simulate withdrawing refrigerant from a vessel:

    $ docker-compose run web python manage.py withdraw

## The problem

We have a refrigerant vessel with a starting content of 50 Kg. Our withdraw script simulates two users entering a 10 Kg withdrawal on the same vessel.

However, it seems that only one of those is being registered as the vessel is being emptied by 10 Kg on each run instead of the expected 20 Kg. Can you find the bug and solve it?

## Bonus - Useability upgrade

Currently, even if the vessel is empty, users can still attempt to withdraw from it, resulting in a database exception. Although our database schema prevents negative values, we aim to enhance user experience by displaying a clearer message in the withdrawal script. This message should notify users that the vessel is empty and further withdrawals are not possible. Can you improve the useability of this script?

Happy debugging!
