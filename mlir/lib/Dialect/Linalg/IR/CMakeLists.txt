add_mlir_dialect_library(MLIRLinalg
  LinalgInterfaces.cpp
  LinalgOps.cpp
  LinalgDialect.cpp

  ADDITIONAL_HEADER_DIRS
  ${MLIR_MAIN_INCLUDE_DIR}/mlir/Dialect/Linalg

  DEPENDS
  MLIRLinalgInterfacesIncGen
  MLIRLinalgOpsIncGen
  MLIRLinalgStructuredOpsIncGen

  LINK_LIBS PUBLIC
  MLIRAffine
  MLIRArithmetic
  MLIRBufferization
  MLIRDialectUtils
  MLIRInferTypeOpInterface
  MLIRIR
  MLIRParser
  MLIRSideEffectInterfaces
  MLIRSCF
  MLIRMath
  MLIRMemRef
  MLIRTensor
  MLIRTilingInterface
  MLIRViewLikeInterface
  )
