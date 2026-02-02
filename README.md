# program-107
import sqlite3

# Connect to the SQLite database
conn = sqlite3.connect('mydatabase.db')

# Create a backup file
backup_file = 'mydatabase_backup.sql'

with open(backup_file, 'w', encoding='utf-8') as f:
    for line in conn.iterdump():
        f.write(f'{line}\n')

print('Backup performed successfully.')
print(f'Saved as {backup_file}')

# Close the connection
conn.close()
output
Backup performed successfully.
Saved as mydatabase_backup.sql
