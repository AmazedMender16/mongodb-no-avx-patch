# Build MongoDB for non-AVX CPUs

**Overview**

This repository contains a patch for MongoDB that modifies the build process to remove AVX/AVX2 support. This patch is intended to help users who need to compile MongoDB without AVX/AVX2 support due to hardware or compatibility issues.


**Purpose**

The primary goal of this patch is to ensure MongoDB can be compiled and run on systems that do not support AVX/AVX2 instructions. The patch modifies specific files in the MongoDB source code and adjusts build flags to avoid AVX/AVX2 instructions.


**Installation**

To apply the patch and build MongoDB, follow these steps:

1. **Clone the MongoDB Repository**:
```
git clone --branch r7.0.14 https://github.com/mongodb/mongo.git
cd mongo
```
2. **Apply the Patch**: Place the patch file (e.g., mongodb-avx2.patch) in the root of the MongoDB source directory and apply it using the patch command:
```
curl -sfLo mongodb-avx2.patch https://github.com/AmazedMender16/mongodb-no-avx-patch/raw/master/patches/mongodb-avx2.patch
patch -p1 < mongodb-avx2.patch
```

**Build MongoDB**

Refer to the official MongoDB build instructions for details on how to build MongoDB from source. Follow the instructions provided there, making sure to use the necessary build flags or environment variables to compile MongoDB with the applied patch.


**License**

This patch is licensed under the MIT License. The original MongoDB code is licensed under the Server Side Public License (SSPL). See the LICENSE file in the MongoDB repository for details on MongoDB's license.


**Disclaimer**

This patch is provided as-is and is intended for use with MongoDB version 7.0. It may not be compatible with other versions or future releases of MongoDB. Use it at your own risk and consult MongoDB's documentation for more details.


**Contribution**

Contributions are welcome. If you have suggestions or improvements, please submit a pull request or open an issue.
