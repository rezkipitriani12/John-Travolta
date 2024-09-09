def hitung_gaji_mingguan(jam_kerja, rate_normal=15000):
    # Menghitung gaji normal dan lembur
    if jam_kerja <= 40:
        gaji = jam_kerja * rate_normal
    else:
        jam_lembur = jam_kerja - 40
        rate_lembur = rate_normal * 1.5
        gaji_normal = 40 * rate_normal
        gaji_lembur = jam_lembur * rate_lembur
        gaji = gaji_normal + gaji_lembur
    return gaji

# Input jam kerja Mr. John
jam_kerja = 52  # Sesuai contoh soal

# Hitung gaji
gaji_mingguan = hitung_gaji_mingguan(jam_kerja)

# Output hasil
print(f"Gaji Mr. John minggu ini: Rp {gaji_mingguan}")
