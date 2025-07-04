## `sapmachine:17-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:067eb1acdcecab6d074d1dbcb1c690e3ddaa6b1035b69b6751962274bab714e8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:9b83f8b0ae0cfea9e1abe29f5ab5b9d8d44bea450fad86564dc9128e80a6abb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228329526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8147fe229909a796c0149dc8296c06039accf9f87faf6bec66e001e7d9df0e34`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a619a1883ad6243883df34c78dd1c6f691042f88b69cd5d2396287dccf0721f`  
		Last Modified: Wed, 02 Jul 2025 21:21:44 GMT  
		Size: 198.8 MB (198793840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f75a8d89c00f048dcf5c29f833e1492f21bbf279d0ca35b1097a3515f7d15e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1125554a1c14ce5392ce0ab68a729158a5329e7892b0ffa2f779d0c90f9396c`

```dockerfile
```

-	Layers:
	-	`sha256:f5466aaf0f5603b5028e6b1ab04f7087592175feac8ab9ab26a80f9da76b1c43`  
		Last Modified: Wed, 02 Jul 2025 06:05:33 GMT  
		Size: 2.4 MB (2375751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35cee708b7b2434b9f0c7a0e3a533e52a85f6c4eec3d86fb71bb1467f9f2c179`  
		Last Modified: Wed, 02 Jul 2025 06:05:33 GMT  
		Size: 8.9 KB (8933 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:26d8cf0e591904e47dfebfa706abafe4910b68ecde4bb0f6e2c1fa8495ee5325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.9 MB (224865686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d4bc7bb296e40c8cc002d0aac43bef1468fd9dccc1109970c9a523bedebdd11`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0abc7ee1d0149bad8e7ccefd192546f48dd3a65e125e4cec14a4b3aea3b515`  
		Last Modified: Fri, 04 Jul 2025 16:36:54 GMT  
		Size: 197.5 MB (197506414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:b56a5508ad119851e8c0c9bc8f479102f2f16fed3886fecd960707d4195ea8d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3961b0fed38ba6dbba287103b0b939139eaca27d23623ef28a741ea25d14df`

```dockerfile
```

-	Layers:
	-	`sha256:4d2542f9af9e92733dd1f36f676219df8b669c1b3c8d933104ebedb0ef377911`  
		Last Modified: Wed, 02 Jul 2025 09:04:51 GMT  
		Size: 2.4 MB (2375423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0f6501ea38e3fc851c9431f6e50918e98c90e32b40f7b4c04afcf1e7eec0e32`  
		Last Modified: Wed, 02 Jul 2025 09:04:52 GMT  
		Size: 9.0 KB (9034 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:4bb5bafaed26ed0adb7b867a340b472ecff0f3f45b719a280306fa60a2ba9110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234129575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0aa71241246f73143295266fcf45c40adaf17b1f28b2a9502c25629277193f8e`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:41 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:41 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:41 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:41 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.15 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Apr 2025 10:34:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57225c71b3fdbec5aad4735cbc804a952631e1b8ce039ab773ba18bacde2c264`  
		Last Modified: Wed, 02 Jul 2025 05:04:59 GMT  
		Size: 199.7 MB (199686954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:373ddaeca9e87201315a247e3172ad077a982e5dfa9369b5e3dcf0afd34b7571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d79c8946d4ed4a615c85c4a8338bc5f897db042df0825dba1236a8ab2358310`

```dockerfile
```

-	Layers:
	-	`sha256:d8d6a48b97a5cbffac900b46ded0b6dd5239212756bc76e0de62dbe83371596f`  
		Last Modified: Wed, 02 Jul 2025 06:05:42 GMT  
		Size: 2.4 MB (2377846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f20563791e756ae7cf6f7d8e118e9e6f43c490c16add8f928a4b51c901c6bf9d`  
		Last Modified: Wed, 02 Jul 2025 06:05:43 GMT  
		Size: 9.0 KB (8977 bytes)  
		MIME: application/vnd.in-toto+json
