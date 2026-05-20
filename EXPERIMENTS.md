# Experiment Log

Catat setiap percobaan hyperparameter di sini. **Minimal 5 eksperimen.**

> Tips: ubah **satu hyperparameter pada satu waktu** agar bisa mengisolasi efeknya. Setelah memahami efek tiap variabel, baru gabungkan untuk hasil terbaik.

---

## 📋 Tabel Ringkasan

Isi tabel ini setelah selesai semua eksperimen.

| # | Hidden | Neurons | Activation | Optimizer | LR     | Batch | Epochs | Dropout | Test Acc | Train Time |
|---|--------|---------|------------|-----------|--------|-------|--------|---------|----------|------------|
| 0 | 1      | 64      | relu       | sgd       | 0.01   | 32    | 10     | 0.0     | ~85%     | ~30s       |
| 1 | 2      | 256     | relu       | adam      | 0.001  | 128   | 50     | 0.3     |  ~89%    | 71.4s      |
| 2 | 3      | 128     | relu       | adam      | 0.001  | 32    | 20     | 0.3     |  87.77%  |  108.7     |
| 3 | 4      | 256     | relu       | adam      | 0.001  | 64    | 40     | 0.2     |  89.07%  |   118.9s   |
| 4 | 5       | 256        | elu          | rmsprop          | 0.0005       | 32      | 40       | 0.2        | 88.35%         | 229.5s           |
| 5 |        |         |            |           |        |       |        |         |          |            |

> **Eksperimen #0** = baseline (jangan ubah, ini patokan kalian).

---

## 🧪 Detail Setiap Eksperimen

Gunakan template di bawah untuk SETIAP eksperimen.

---

### Eksperimen #1

**Apa yang diubah dari baseline:**
hidden layer jadi 2, neuron 256, optimizer Adam, dropout 0.3, batch 128, epochs 50.

**Hipotesis sebelum run:**
Model lebih dalam + Adam akan meningkatkan akurasi signifikan.

**Hasil:**
- Test accuracy: ~89%
- Train accuracy: ~92%
- Validation accuracy: ~89%
- Train time: 71.4 detik
- Apakah overfit/underfit? relatif seimbang.

**Observasi & Insight:**
Adam + lebih banyak neuron efektif, tapi batch besar bikin training cepat.

**Rencana eksperimen berikutnya:**
coba batch lebih kecil untuk generalisasi.

---

### Eksperimen #2

**Apa yang diubah:**
hidden layer 3, neuron 128, batch 32, epochs 20.

**Hipotesis:**
Batch kecil akan menurunkan loss dan meningkatkan generalisasi.

**Hasil:**  
- Test accuracy: 87.77%
- Train accuracy: ~91%
- Validation accuracy: ~88%
- Train time: 108.7 detik
- Apakah overfit/underfit? sedikit underfit (akurasi test lebih rendah).

**Observasi:**
Batch kecil membantu stabilitas, tapi neuron lebih sedikit menurunkan kapasitas.

**Rencana eksperimen berikutnya:**
tambah neuron lagi.
---

### Eksperimen #3

**Apa yang diubah:**
batch 64, epochs 40, dropout 0.2.

**Hipotesis:**
Training lebih lama + dropout lebih rendah akan meningkatkan akurasi.

**Hasil:**  
- Test accuracy: 89.07%
- Train accuracy: 91.90%
- Validation accuracy: 90.07%
- Train time: 118.9 detik
- Apakah overfit/underfit? sehat, gap kecil.

**Observasi:**
Kombinasi ini paling seimbang sejauh ini.

**Rencana eksperimen berikutnya:**
coba optimizer lain.
---

### Eksperimen #4

**Apa yang diubah:**
hidden layer 5, activation elu, optimizer rmsprop, LR 0.0005.

**Hipotesis:**
ELU + RMSprop akan menurunkan loss.

**Hasil:**  
- Test accuracy: 88.35%
- Train accuracy: ~91%
- Validation accuracy: ~89%
- Train time: 229.5 detik
- Apakah overfit/underfit? sedikit overfit.

**Observasi:**
ELU membantu stabilitas, tapi terlalu banyak layer bikin training lama.

**Rencana eksperimen berikutnya:**
coba 5 layer dengan setting mirip.
---

### Eksperimen #5

**Apa yang diubah:**

**Hipotesis:**

**Hasil:**  
- Test accuracy: ___%
- Train accuracy: ___%
- Validation accuracy: ___%
- Train time: ___ detik
- Apakah overfit/underfit? ___

**Observasi:**

---

## 🏆 Konfigurasi Terbaik

Setelah semua eksperimen, salin konfigurasi terbaik kalian ke sini:

```python
HIDDEN_LAYERS     = ?
NEURONS_PER_LAYER = ?
ACTIVATION        = ?
DROPOUT_RATE      = ?
OPTIMIZER         = ?
LEARNING_RATE     = ?
BATCH_SIZE        = ?
EPOCHS            = ?
```

**Test accuracy final: ___%**
