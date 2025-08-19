# UPF-Calculator
UPF calculator, only transmittance is required

How to use:
python UPF.py your_file.xlsx --use-pvlib --wl nm --T T --step 1
your_file.xlsx is your data file. Example:<img width="248" height="137" alt="image" src="https://github.com/user-attachments/assets/248dab74-eb79-455a-9038-ab122404c46f" />
=======================================================================

Calculated in accordance with AS/NZS 4399:1996. E(λ) is taken from ASTM G-173-03 (the standard ground-level solar spectrum), and ε(λ) is computed using the CIE erythemal formula (McKinlay & Diffey, 1987).

Input: CSV or Excel file, containing at least:
Wavelength column (default name: 'nm', unit: nm, recommended interval: 1 nm)
Transmittance T column (default name: 'T', values can be either 0–1 or 0–100%, automatically detected.
If the transmittance is given in percentage form (e.g., 85 meaning 85%), the maximum value will exceed 1, and the script will automatically divide by 100 to convert it into the 0–1 range.)



采用AS/NZS 4399:1996标准，其中E(λ)为ASTM G‑173‑03（标准地面太阳光谱），ε(λ)采用CIE erythemal 公式（McKinlay & Diffey, 1987）计算

输入：CSV 或 Excel，至少包含：
- 波长列（默认名称 'nm'，单位 nm，建议 1 nm 间隔）
- 透射比 T 列（默认 'T'，可为 0–1 或 0–100%，可自动检测，如果
透过率是百分数形式（比如85表示85%），最大值会大于1，于是脚本会自动除以 100 转换到 0–1 区间。）

用法：
    python UPF.py your_file.xlsx --use-pvlib --wl nm --T T --step 1
