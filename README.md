# Diagonal gauging in six-dimensional supergravity

Supplementary catalogues and a self-contained Mathematica notebook for diagonal U(1)R+ and Sp(1)R+ gauging with one or two additional simple group factors.

## Files

- [DG_search.nb](DG_search.nb): the anomaly search and spectrum explorer, with two button-driven panels. No companion code files or external Lie-algebra package are required.
- [q=2_tables.pdf](q%3D2_tables.pdf): catalogue with exact maximum absolute hyperino charge q_max = 2, for one or two additional factors. The one-factor A3 catalogue is omitted from this PDF because of its size; the notebook can compute it.
- [d=3_tables.pdf](d%3D3_tables.pdf): catalogue with exact maximum occupied Sp(1)R+ representation dimension d_max = 3, for one or two additional factors.

## Open and initialize the notebook

Open **DG_search.nb** in Mathematica, enable dynamic content if prompted, and click **Initialize notebook**. Initialization loads the definitions and opens the panels; it does not start a search.

Use a fresh kernel, or save unrelated kernel work first: initialization clears existing definitions in Mathematica's Global context. Click **Initialize notebook** again after restarting the kernel.

## Panel 1: find spectra

Choose **U(1)** or **Sp(1)**, **one or two additional groups**, the group names, and the **exact q_max or d_max**. Click **Find spectra** to display the spectrum and class counts, anomaly vectors, lattice types, and matter spectra.

The maximum selects an exact sector: q_max = 2 means the spectrum contains charge magnitude 2; lower charges may also occur. Likewise, d_max = 3 means the largest occupied Sp(1) representation has dimension 3. The neutral U(1) sector uses q_max = 0; the Sp(1) singlet sector uses d_max = 1.

Group names use Cartan type and rank: A5 = SU(6), C4 = Sp(4), and D6 = Spin(12). Enter only the additional factors; the chosen diagonal R-symmetry factor is supplied automatically. Dropdowns show the supported search scope: one factor has rank 3-30, or is G2; D starts at D4. For two factors, each has rank 5-30, or is F4.

The table is paged, with stable spectrum numbers. Changing a search option clears the previous result. Larger groups and maxima can require substantial computation.

## Panel 2: inspect all allocations

Click **Select** beside a spectrum, or enter its spectrum number. For U(1), click **Show all charge allocations** to list every cubic-compatible allocation counted by **N_sign**, with the irrep labels fixed and simultaneous reversal of all charges counted once. Self-conjugate blocks have no independent charge-sign choice. The first allocation matches the spectrum table.

For Sp(1), click **Show complete dimension allocation** to display the complete diagonal-irrep allocation; there are no independent U(1) charge signs. **Open complete list in a new notebook** opens the full output in a separate notebook. Paging does not reduce the number of computed allocations.

## Scope and citation

These materials cover anomaly cancellation, spectrum checks, and spectrum enumeration. They do not include the Minkowski-vacuum calculations or code. Please cite the accompanying paper when using these materials. Corrections and questions are welcome through GitHub Issues.

The panel notebook was verified in Mathematica 13.2.1, including G2 with U(1), q_max = 2 (9 spectra, 8 classes, sum N_sign = 9), A6 x D9 with U(1), q_max = 2 (8 spectra, 6 classes, sum N_sign = 37; spectrum 8 has 14 allocations), C4 with Sp(1), d_max = 3 (3 spectra, 3 classes), and A5 x D6 with Sp(1), d_max = 3 (5 spectra, 5 classes).
