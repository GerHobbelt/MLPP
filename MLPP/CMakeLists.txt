project(MLPP)

SET(SOURCE_FILES
  Stat/Stat.cpp
  LinAlg/LinAlg.cpp
  Regularization/Reg.cpp
  Activation/Activation.cpp
  Utilities/Utilities.cpp
  Data/Data.cpp
  Cost/Cost.cpp
  ANN/ANN.cpp
  HiddenLayer/HiddenLayer.cpp
  OutputLayer/OutputLayer.cpp
  MLP/MLP.cpp
  LinReg/LinReg.cpp
  LogReg/LogReg.cpp
  UniLinReg/UniLinReg.cpp
  CLogLogReg/CLogLogReg.cpp
  ExpReg/ExpReg.cpp
  ProbitReg/ProbitReg.cpp
  SoftmaxReg/SoftmaxReg.cpp
  TanhReg/TanhReg.cpp
  SoftmaxNet/SoftmaxNet.cpp
  Convolutions/Convolutions.cpp
  AutoEncoder/AutoEncoder.cpp
  MultinomialNB/MultinomialNB.cpp
  BernoulliNB/BernoulliNB.cpp
  GaussianNB/GaussianNB.cpp
  KMeans/KMeans.cpp
  kNN/kNN.cpp
  PCA/PCA.cpp
  OutlierFinder/OutlierFinder.cpp
  MANN/MANN.cpp
  MultiOutputLayer/MultiOutputLayer.cpp
  SVC/SVC.cpp
  NumericalAnalysis/NumericalAnalysis.cpp
  DualSVC/DualSVC.cpp
  Transforms/Transforms.cpp
)

add_library(${PROJECT_NAME}
	${SOURCE_FILES}
	)

target_compile_definitions(${PROJECT_NAME} PRIVATE _USE_MATH_DEFINES)
target_include_directories(${PROJECT_NAME} PUBLIC
	$<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
    $<BUILD_INTERFACE:${CMAKE_CURRENT_BINARY_DIR}>)