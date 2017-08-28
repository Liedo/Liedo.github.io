# Structure of the library

The code is structured as follows... (to be completed)

```javascript
public void example() {
TsData[] series = {benchmark, model, target};
boolean twoSided = true;
double rmse = new double ;
double dmPval = new double ;
double bias = new double ;
double biasPval = new double ;
double arcorr = new double ;
double arPval = new double ;
double m_enc_bench = new double ;
double m_enc_bench_Pval = new double ;
double bench_enc_m = new double ;
double bench_enc_m_Pval = new double ;
// squared root of T
int bandwith = (int) Math.pow(series.getObsCount(), 1.0 / 2.0);
GlobalForecastingEvaluation eval = new GlobalForecastingEvaluation(model, benchmark,
target,
AccuracyTests.AsymptoticsType.HAR_FIXED_B);
eval.getDieboldMarianoTest().setBandwith(bandwith);
dmPval = eval.getDieboldMarianoTest().getPValue(twoSided);
ForecastEvaluation feval = new ForecastEvaluation(model, benchmark, target);
rmse = feval.calcRMSE();
eval.getBiasTest().setBandwith(bandwith);
bias = eval.getBiasTest().getAverageLoss();
biasPval = eval.getBiasTest().getPValue(twoSided);
eval.getEfficiencyTest().setBandwith(bandwith);
arcorr = eval.getEfficiencyTest().calcCorelation();
arPval = eval.getEfficiencyTest().getPValue(twoSided);
eval.getModelEncompassesBenchmarkTest().setBandwith(bandwith);
m_enc_bench = eval.getModelEncompassesBenchmarkTest().calcWeights();
m_enc_bench_Pval = eval.getModelEncompassesBenchmarkTest().getPValue(twoSided);
bench_enc_m = eval.getBenchmarkEncompassesModelTest().calcWeights();
bench_enc_m_Pval = eval.getBenchmarkEncompassesModelTest().getPValue(twoSided);
}
```

### [Notation](notation.md)
### [Diebold-Mariano Test](dmtest.md)
### [Encompassing Test](encompassing.md)
### [Bias and Efficiency](bias.md)
### [Implementation in JDemetra+](jdimplementation.md)