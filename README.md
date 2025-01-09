# dayz-scripts

**Script to capture player position by id (bohemia):** <br />
```./player_get_position.sh AbcDefGhiJ-1_-A7b8C1Def04G4hi1JKLMn2OpqRStu= <br />
DB Version - 0200 <br />
Position X - 6DF92E46 => 11198.356 <br />
Position Z - 57E72C42 => 43.225918 <br />
Position Y - 33BA6046 => 14382.55 <br /><br />```

**Script to replace the player position by id (bohemia) passing the coordinates X, Z and Y (the player must be logged out because upon logout the player database is updated with their last position):** <br />
./player_replace_position.sh AbcDefGhiJ-1_-A7b8C1Def04G4hi1JKLMn2OpqRStu= 1594.6315 299.88126 9088.511 <br />
/tmp/dayz/AbcDefGhiJ-1_-A7b8C1Def04G4hi1JKLMn2OpqRStu= <br />
total 2.4M <br />
-rw-r--r-- 1 root      root      2.4M Jan  8 22:02 players_bkp.db <br />
-rw-r--r-- 1 root      root      9.3K Jan  8 22:02 update_bkp.sql <br />
-rw-r--r-- 1 root      root      9.2K Jan  8 22:02 update.sql <br /><br />

To execute a rollback: sqlite3 /home/fastadmin/servers/dayz-server/mpmissions/dayzOffline.chernarusplus/storage_1/players.db < /tmp/dayz/AbcDefGhiJ-1_-A7b8C1Def04G4hi1JKLMn2OpqRStu=/update_bkp.sql
