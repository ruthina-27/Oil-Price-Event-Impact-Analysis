# Oil Price Event Impact Analysis - Data Analysis Workflow

## Project Overview
This project analyzes the impact of major geopolitical and economic events on Brent oil prices using Bayesian Change Point Detection methods. The goal is to identify statistically significant structural breaks in oil price time series and correlate them with known events.

## 1. Data Analysis Workflow

### Phase 1: Data Preparation and Exploration
1. **Data Loading and Validation**
   - Load Brent oil price time series data (1987-2024)
   - Validate data quality (missing values, outliers, date consistency)
   - Perform initial exploratory data analysis

2. **Event Data Compilation**
   - Research and compile major geopolitical/economic events
   - Create structured dataset with event dates and descriptions
   - Validate event relevance and timing accuracy

3. **Data Preprocessing**
   - Handle missing values and outliers
   - Ensure consistent date formatting
   - Create time-aligned datasets for analysis

### Phase 2: Statistical Analysis Foundation
1. **Time Series Analysis**
   - Test for stationarity using Augmented Dickey-Fuller test
   - Calculate rolling statistics (mean, standard deviation)
   - Identify basic patterns and trends

2. **Change Point Detection Setup**
   - Define Bayesian change point model structure
   - Set appropriate priors based on domain knowledge
   - Establish model validation criteria

### Phase 3: Bayesian Change Point Analysis
1. **Model Implementation**
   - Implement PyMC3 change point detection model
   - Configure MCMC sampling parameters
   - Run multiple chains for convergence validation

2. **Change Point Identification**
   - Extract posterior distributions of change points
   - Calculate credible intervals for change point locations
   - Rank change points by statistical significance

### Phase 4: Event-Impact Correlation
1. **Temporal Alignment**
   - Map detected change points to event timeline
   - Calculate time lags between events and change points
   - Identify potential causal relationships

2. **Impact Quantification**
   - Measure magnitude of price changes at change points
   - Calculate statistical significance of impacts
   - Categorize events by impact strength

### Phase 5: Validation and Insights
1. **Model Validation**
   - Cross-validate results using different time periods
   - Compare with alternative change point methods
   - Assess model robustness

2. **Business Intelligence**
   - Generate actionable insights for oil market participants
   - Create risk assessment framework
   - Develop predictive indicators

## 2. Key Concepts and Methodology

### Bayesian Change Point Detection
- **Concept**: Identifies structural breaks in time series where underlying parameters change
- **Advantages**: 
  - Provides uncertainty quantification
  - Incorporates prior knowledge
  - Handles multiple change points simultaneously
- **Implementation**: Uses PyMC3 for probabilistic programming

### Event Selection Criteria
Events were selected based on:
1. **Geopolitical Significance**: Major conflicts, sanctions, political upheavals
2. **Economic Impact**: Financial crises, major policy changes
3. **Supply/Demand Shocks**: OPEC decisions, production disruptions
4. **Market Structure Changes**: New technologies, regulatory changes

### Statistical Validation Framework
- **Convergence Diagnostics**: Gelman-Rubin statistic, effective sample size
- **Model Comparison**: Deviance Information Criterion (DIC)
- **Sensitivity Analysis**: Prior specification robustness

## 3. Expected Outcomes and Deliverables

### Primary Deliverables
1. **Interactive Dashboard**: Real-time visualization of change points and events
2. **Statistical Report**: Detailed analysis of event impacts
3. **Predictive Model**: Framework for anticipating future price impacts

### Key Insights Expected
1. **Event Impact Ranking**: Which events had the strongest price effects
2. **Temporal Patterns**: How quickly markets react to different event types
3. **Risk Assessment**: Probability of significant price movements post-events

## 4. Success Metrics

### Technical Metrics
- Model convergence (R-hat < 1.1)
- Effective sample size > 1000
- Credible interval coverage

### Business Metrics
- Identification of 80%+ of known major price movements
- False positive rate < 20%
- Actionable insights for 70%+ of analyzed events

## 5. Risk Mitigation

### Technical Risks
- **Model Convergence**: Multiple chains, longer sampling
- **Prior Sensitivity**: Robustness checks with different priors
- **Data Quality**: Comprehensive validation procedures

### Business Risks
- **Overfitting**: Cross-validation and out-of-sample testing
- **Interpretation Errors**: Expert review and validation
- **Timing Uncertainty**: Multiple event date scenarios

## 6. Timeline and Milestones

### Week 1: Foundation
- [x] Data compilation and validation
- [x] Initial exploratory analysis
- [x] Basic change point model implementation

### Week 2: Core Analysis
- [ ] Advanced Bayesian modeling
- [ ] Change point detection and validation
- [ ] Event-impact correlation analysis

### Week 3: Insights and Dashboard
- [ ] Statistical significance testing
- [ ] Dashboard development
- [ ] Report generation

### Week 4: Validation and Delivery
- [ ] Model validation and robustness checks
- [ ] Final insights compilation
- [ ] Project delivery and documentation 