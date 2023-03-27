# PathogenVariantModels

Practical in the Bayesian inference methods for infectious diseases research workshop at Uni Cambridge.

Conducted by Dr David Pascall and Joshua Blake, script is adapted from their code examples.

**Question**: How does viral load vary over individuals and the course of infection?

**Dataset**: ATACCC: daily PCR testing of exposed individuals
- assume that cycle threshold value from PCR is proprotional to log viral load
- max CT value can be observed is 40

**Challenges**:
- some infections only minimally observed
- want to gneralise to what unseen indviduals loo like
- false negatives and limit of detection
	- negative result does not mean absence of virus

**Solution**:
- hierarchial model: assume that individuals are "similar"
	- "random effects" / "mixed model"
	- after parameters estimate, can simulate unseen individuals
- Bayesian paradigm: natural inclusion of false negative results

**Simple mode**l:
- piecewise linear model
- good approximation to more mechanistic ODE-based models