# Hamiltonian-Dataset-of-Range-Tuned-QM9-Conjugated-Molecules
A dataset of conjugated molecules from QM9 with range-tuned functional calculations, including Hamiltonian matrices, orbital energies, and overlap matrices, etc.

## Dataset URL
The dataset is available at Zenodo(https://zenodo.org/records/14906024)

## Dataset Usage :

```python
import sqlite3

conn = sqlite3.connect('qm9_conj_OT-w.db') 
cursor = conn.cursor()

cursor.execute("SELECT * FROM qm9_data WHERE i = 0")
molecule_data = cursor.fetchone()

smiles = molecule_data[1]
omega = molecule_data[2] 

conn.close()
