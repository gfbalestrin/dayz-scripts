# dayz-scripts

Script to capture player position by id (bohemia):
./player_get_position.sh AbcDefGhiJ-1_-A7b8C1Def04G4hi1JKLMn2OpqRStu=
DB Version - 0200
Position X - 6DF92E46 => 11198.356
Position Z - 57E72C42 => 43.225918
Position Y - 33BA6046 => 14382.55

Script to replace the player position by id (bohemia) passing the coordinates X, Z and Y (the player must be logged out because upon logout the player database is updated with their last position):
./player_replace_position.sh AbcDefGhiJ-1_-A7b8C1Def04G4hi1JKLMn2OpqRStu= 1594.6315 299.88126 9088.511
/tmp/dayz/AbcDefGhiJ-1_-A7b8C1Def04G4hi1JKLMn2OpqRStu=
total 2.4M
-rw-r--r-- 1 root      root      2.4M Jan  8 22:02 players_bkp.db
-rw-r--r-- 1 root      root      9.3K Jan  8 22:02 update_bkp.sql
-rw-r--r-- 1 root      root      9.2K Jan  8 22:02 update.sql

To execute a rollback: sqlite3 /home/fastadmin/servers/dayz-server/mpmissions/dayzOffline.chernarusplus/storage_1/players.db < /tmp/dayz/AbcDefGhiJ-1_-A7b8C1Def04G4hi1JKLMn2OpqRStu=/update_bkp.sql
