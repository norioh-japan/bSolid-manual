# bSolid マニュアル - AI支援メンテナンス管理システム

**ファイル名**: `08-05_ai_maintenance_system.md`  
**カテゴリ**: 装備管理 - AI支援メンテナンス  
**関連**: 装備概要、構造、IoT統合

---

## 📋 **概要**

bSolidのAI支援メンテナンス管理システムは、機械学習と人工知能を活用して、装備の予測保全、自動故障診断、最適な保守計画を実現します。これにより、計画外停止の削減、メンテナンスコストの最適化、機械稼働率の最大化を実現します。

---

## 🤖 **AI支援メンテナンス システム**

### **1. 予測保全エンジン**

#### **システム構成**
```python
class PredictiveMaintenanceEngine:
    def __init__(self):
        self.sensor_analyzer = SensorDataAnalyzer()
        self.failure_predictor = FailurePredictionModel()
        self.maintenance_optimizer = MaintenanceOptimizer()
        self.alert_manager = AlertManager()
    
    def predict_maintenance_needs(self, equipment_data):
        # センサーデータ分析
        sensor_patterns = self.sensor_analyzer.analyze_patterns(equipment_data)
        
        # 故障予測
        failure_probability = self.failure_predictor.predict(sensor_patterns)
        
        # 最適メンテナンス計画
        maintenance_plan = self.maintenance_optimizer.optimize(failure_probability)
        
        return maintenance_plan
```

#### **予測アルゴリズム**
```python
# 故障予測モデル
class FailurePredictionModel:
    def __init__(self):
        self.models = {
            'vibration_analysis': VibrationAnalysisModel(),
            'temperature_monitoring': TemperatureModel(),
            'current_signature': CurrentSignatureModel(),
            'acoustic_analysis': AcousticAnalysisModel()
        }
    
    def predict_failure_probability(self, sensor_data):
        predictions = {}
        
        for component, model in self.models.items():
            # 各センサーデータから故障確率を計算
            probability = model.predict_probability(sensor_data[component])
            predictions[component] = {
                'failure_probability': probability,
                'remaining_useful_life': model.estimate_rul(sensor_data[component]),
                'confidence_level': model.get_confidence(sensor_data[component])
            }
        
        # 統合故障予測
        integrated_prediction = self.integrate_predictions(predictions)
        return integrated_prediction
```

### **2. 自動故障診断システム**

#### **診断エンジン**
```python
class AutomaticDiagnosticEngine:
    def __init__(self):
        self.symptom_analyzer = SymptomAnalyzer()
        self.diagnostic_rules = DiagnosticRuleEngine()
        self.knowledge_base = MaintenanceKnowledgeBase()
        self.ml_classifier = FaultClassificationModel()
    
    def diagnose_fault(self, symptom_data, equipment_info):
        # 症状分析
        analyzed_symptoms = self.symptom_analyzer.analyze(symptom_data)
        
        # ルールベース診断
        rule_based_diagnosis = self.diagnostic_rules.evaluate(analyzed_symptoms)
        
        # 機械学習による分類
        ml_diagnosis = self.ml_classifier.classify(symptom_data)
        
        # 知識ベース検索
        knowledge_suggestions = self.knowledge_base.search_solutions(analyzed_symptoms)
        
        # 統合診断結果
        final_diagnosis = self.integrate_diagnoses(
            rule_based_diagnosis, ml_diagnosis, knowledge_suggestions
        )
        
        return final_diagnosis
```

#### **故障パターン認識**
```javascript
// 故障パターン分析
const FaultPatternRecognition = {
    patterns: {
        mechanical_wear: {
            indicators: ['increasing_vibration', 'temperature_rise', 'current_fluctuation'],
            severity_thresholds: {
                warning: 0.6,
                critical: 0.8,
                emergency: 0.9
            },
            recommended_actions: [
                'schedule_inspection',
                'order_replacement_parts',
                'plan_downtime'
            ]
        },
        
        electrical_fault: {
            indicators: ['voltage_anomaly', 'current_spike', 'insulation_resistance'],
            severity_thresholds: {
                warning: 0.5,
                critical: 0.7,
                emergency: 0.85
            },
            recommended_actions: [
                'electrical_inspection',
                'contact_specialist',
                'immediate_shutdown'
            ]
        }
    },
    
    recognizePattern(sensorData) {
        const detectedPatterns = [];
        
        for (const [patternName, pattern] of Object.entries(this.patterns)) {
            const matchScore = this.calculateMatchScore(sensorData, pattern.indicators);
            
            if (matchScore > pattern.severity_thresholds.warning) {
                detectedPatterns.push({
                    pattern: patternName,
                    severity: this.determineSeverity(matchScore, pattern.severity_thresholds),
                    confidence: matchScore,
                    recommendations: pattern.recommended_actions
                });
            }
        }
        
        return detectedPatterns;
    }
};
```

### **3. 最適保守計画システム**

#### **保守最適化エンジン**
```python
class MaintenanceOptimizationEngine:
    def __init__(self):
        self.cost_calculator = MaintenanceCostCalculator()
        self.schedule_optimizer = ScheduleOptimizer()
        self.resource_manager = ResourceManager()
        self.constraint_handler = ConstraintHandler()
    
    def optimize_maintenance_schedule(self, equipment_list, constraints):
        # コスト分析
        cost_analysis = self.cost_calculator.analyze_costs(equipment_list)
        
        # リソース可用性確認
        resource_availability = self.resource_manager.check_availability()
        
        # 制約条件処理
        processed_constraints = self.constraint_handler.process(constraints)
        
        # 最適スケジュール生成
        optimal_schedule = self.schedule_optimizer.optimize(
            equipment_list, cost_analysis, resource_availability, processed_constraints
        )
        
        return optimal_schedule
```

#### **動的スケジューリング**
```python
# 動的保守スケジューリング
class DynamicMaintenanceScheduler:
    def __init__(self):
        self.priority_calculator = PriorityCalculator()
        self.impact_assessor = ImpactAssessor()
        self.resource_allocator = ResourceAllocator()
    
    def dynamic_reschedule(self, current_schedule, new_events):
        updated_schedule = current_schedule.copy()
        
        for event in new_events:
            # 優先度計算
            priority = self.priority_calculator.calculate(event)
            
            # 影響度評価
            impact = self.impact_assessor.assess_impact(event, current_schedule)
            
            # リソース再配分
            resource_allocation = self.resource_allocator.reallocate(
                event, priority, impact
            )
            
            # スケジュール更新
            updated_schedule = self.update_schedule(
                updated_schedule, event, resource_allocation
            )
        
        return updated_schedule
```

---

## 📊 **機械学習モデル**

### **1. 故障予測モデル**

#### **LSTM時系列予測**
```python
import tensorflow as tf
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import LSTM, Dense, Dropout

class FailurePredictionLSTM:
    def __init__(self, sequence_length=50, features=10):
        self.sequence_length = sequence_length
        self.features = features
        self.model = self.build_model()
    
    def build_model(self):
        model = Sequential([
            LSTM(128, return_sequences=True, input_shape=(self.sequence_length, self.features)),
            Dropout(0.2),
            LSTM(64, return_sequences=True),
            Dropout(0.2),
            LSTM(32),
            Dropout(0.2),
            Dense(16, activation='relu'),
            Dense(1, activation='sigmoid')  # 故障確率
        ])
        
        model.compile(
            optimizer='adam',
            loss='binary_crossentropy',
            metrics=['accuracy', 'precision', 'recall']
        )
        
        return model
    
    def predict_failure_probability(self, sensor_sequence):
        """センサー時系列データから故障確率を予測"""
        normalized_data = self.normalize_data(sensor_sequence)
        prediction = self.model.predict(normalized_data)
        return float(prediction[0][0])
```

#### **アンサンブル予測**
```python
# アンサンブル故障予測システム
class EnsembleFailurePrediction:
    def __init__(self):
        self.models = {
            'lstm': FailurePredictionLSTM(),
            'random_forest': RandomForestFailureModel(),
            'svm': SVMFailureModel(),
            'xgboost': XGBoostFailureModel()
        }
        self.weights = {
            'lstm': 0.4,
            'random_forest': 0.25,
            'svm': 0.15,
            'xgboost': 0.2
        }
    
    def ensemble_predict(self, sensor_data):
        predictions = {}
        
        for model_name, model in self.models.items():
            prediction = model.predict(sensor_data)
            predictions[model_name] = prediction
        
        # 重み付き平均
        weighted_prediction = sum(
            predictions[model] * self.weights[model] 
            for model in predictions
        )
        
        # 信頼度計算
        confidence = self.calculate_confidence(predictions)
        
        return {
            'failure_probability': weighted_prediction,
            'confidence': confidence,
            'individual_predictions': predictions
        }
```

### **2. 異常検知システム**

#### **オートエンコーダー異常検知**
```python
class AnomalyDetectionAutoencoder:
    def __init__(self, input_dim=20):
        self.input_dim = input_dim
        self.model = self.build_autoencoder()
        self.threshold = None
    
    def build_autoencoder(self):
        # エンコーダー
        encoder = tf.keras.Sequential([
            tf.keras.layers.Dense(16, activation='relu', input_shape=(self.input_dim,)),
            tf.keras.layers.Dense(8, activation='relu'),
            tf.keras.layers.Dense(4, activation='relu')
        ])
        
        # デコーダー
        decoder = tf.keras.Sequential([
            tf.keras.layers.Dense(8, activation='relu', input_shape=(4,)),
            tf.keras.layers.Dense(16, activation='relu'),
            tf.keras.layers.Dense(self.input_dim, activation='linear')
        ])
        
        # 完全なオートエンコーダー
        autoencoder = tf.keras.Sequential([encoder, decoder])
        autoencoder.compile(optimizer='adam', loss='mse')
        
        return autoencoder
    
    def detect_anomaly(self, sensor_data):
        """センサーデータから異常を検知"""
        reconstruction = self.model.predict(sensor_data)
        reconstruction_error = np.mean(np.square(sensor_data - reconstruction), axis=1)
        
        if self.threshold is None:
            return reconstruction_error
        
        anomalies = reconstruction_error > self.threshold
        return {
            'anomaly_detected': anomalies,
            'reconstruction_error': reconstruction_error,
            'anomaly_score': reconstruction_error / self.threshold
        }
```

---

## 📈 **パフォーマンス指標と監視**

### **1. KPI監視システム**

#### **メンテナンス効率指標**
```python
class MaintenanceKPIMonitor:
    def __init__(self):
        self.kpi_calculator = KPICalculator()
        self.trend_analyzer = TrendAnalyzer()
        self.benchmark_comparator = BenchmarkComparator()
    
    def calculate_maintenance_kpis(self, maintenance_data):
        kpis = {
            # 効率性指標
            'mttr': self.kpi_calculator.mean_time_to_repair(maintenance_data),
            'mtbf': self.kpi_calculator.mean_time_between_failures(maintenance_data),
            'availability': self.kpi_calculator.equipment_availability(maintenance_data),
            
            # コスト指標
            'maintenance_cost_ratio': self.kpi_calculator.maintenance_cost_ratio(maintenance_data),
            'cost_per_hour': self.kpi_calculator.cost_per_operating_hour(maintenance_data),
            
            # 品質指標
            'first_time_fix_rate': self.kpi_calculator.first_time_fix_rate(maintenance_data),
            'planned_maintenance_ratio': self.kpi_calculator.planned_vs_reactive_ratio(maintenance_data),
            
            # 予測精度指標
            'prediction_accuracy': self.kpi_calculator.prediction_accuracy(maintenance_data),
            'false_alarm_rate': self.kpi_calculator.false_alarm_rate(maintenance_data)
        }
        
        # トレンド分析
        trends = self.trend_analyzer.analyze_trends(kpis)
        
        # ベンチマーク比較
        benchmarks = self.benchmark_comparator.compare(kpis)
        
        return {
            'kpis': kpis,
            'trends': trends,
            'benchmarks': benchmarks
        }
```

### **2. リアルタイムダッシュボード**

#### **監視ダッシュボード設定**
```javascript
// リアルタイム監視ダッシュボード
const MaintenanceDashboard = {
    widgets: {
        equipment_health: {
            type: 'gauge',
            title: '装備健全性',
            data_source: 'health_score_api',
            update_interval: 5000,
            thresholds: {
                critical: 0.3,
                warning: 0.6,
                good: 0.8
            }
        },
        
        failure_predictions: {
            type: 'timeline',
            title: '故障予測',
            data_source: 'prediction_api',
            update_interval: 30000,
            display_horizon: '30_days'
        },
        
        maintenance_schedule: {
            type: 'calendar',
            title: '保守スケジュール',
            data_source: 'schedule_api',
            update_interval: 60000,
            view_mode: 'weekly'
        },
        
        cost_tracking: {
            type: 'chart',
            title: 'コスト追跡',
            data_source: 'cost_api',
            update_interval: 300000,
            chart_type: 'line'
        }
    },
    
    initializeDashboard() {
        this.setupWebSocketConnection();
        this.createWidgets();
        this.startDataPolling();
    },
    
    updateWidget(widgetId, newData) {
        const widget = this.widgets[widgetId];
        
        switch (widget.type) {
            case 'gauge':
                this.updateGaugeWidget(widgetId, newData);
                break;
            case 'timeline':
                this.updateTimelineWidget(widgetId, newData);
                break;
            case 'calendar':
                this.updateCalendarWidget(widgetId, newData);
                break;
            case 'chart':
                this.updateChartWidget(widgetId, newData);
                break;
        }
    }
};
```

---

## 🔧 **実装・運用ガイド**

### **1. システム導入手順**

#### **段階的導入計画**
```yaml
deployment_phases:
  phase1_foundation:
    duration: "4週間"
    objectives:
      - 基本センサー設置
      - データ収集システム構築
      - 基本分析機能実装
    deliverables:
      - センサーネットワーク
      - データパイプライン
      - 基本ダッシュボード
  
  phase2_intelligence:
    duration: "6週間"
    objectives:
      - AI予測モデル実装
      - 異常検知システム構築
      - 自動アラート機能
    deliverables:
      - 故障予測システム
      - 異常検知エンジン
      - アラート管理システム
  
  phase3_optimization:
    duration: "4週間"
    objectives:
      - 保守計画最適化
      - ワークフロー統合
      - 性能調整
    deliverables:
      - 最適化エンジン
      - 統合ワークフロー
      - 性能レポート
```

### **2. 運用ベストプラクティス**

#### **日常運用手順**
1. **毎日の健全性チェック**
   - ダッシュボード確認
   - アラート状況確認
   - 予測精度検証

2. **週次レビュー**
   - KPI分析
   - 予測精度評価
   - 保守計画調整

3. **月次最適化**
   - モデル再学習
   - システム性能評価
   - 運用改善計画

---

## 📊 **導入効果と ROI**

### **期待される効果**
- **計画外停止削減**: 80%減少
- **メンテナンスコスト削減**: 40%減少
- **機械稼働率向上**: 15%向上
- **故障予測精度**: 90%以上

### **ROI計算例**
```python
def calculate_maintenance_roi(investment_cost, annual_savings):
    """メンテナンスシステムのROI計算"""
    
    savings_breakdown = {
        'reduced_downtime': annual_savings * 0.5,
        'optimized_maintenance': annual_savings * 0.3,
        'extended_equipment_life': annual_savings * 0.2
    }
    
    payback_period = investment_cost / annual_savings
    five_year_roi = ((annual_savings * 5) - investment_cost) / investment_cost * 100
    
    return {
        'annual_savings': annual_savings,
        'savings_breakdown': savings_breakdown,
        'payback_period_years': payback_period,
        'five_year_roi_percent': five_year_roi
    }
```

---

**最終更新**: 2024年12月  
**バージョン**: 2.0  
**言語**: 日本語 
