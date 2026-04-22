## `sapmachine:jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:8c8b96f2996710f0dca639326b1b82ac3f1d39d2328edf42b79ab98a6ce7d2db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:cf251275e661828cce07cd32d87a0b0aa87d4a44f72ec2a630e54e4a22001b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88350600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fbbdbb3a3a8fd674c8a4599aed1c9fbd50d281a6e7d4a6b929434b5e77bcfd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:02:42 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:02:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:02:42 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be35067040572a29b0b346d829db8ba5d314f93480ceb2193a28aed49407bc9`  
		Last Modified: Tue, 21 Apr 2026 23:02:57 GMT  
		Size: 58.6 MB (58614102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c1434badf4ec816c820f2cabd923de0edd3c3b94b846a169cf667b67edfa6ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2561222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1255865dfd6461eba45b6023f90339f636b18d03616be79e1c96254a6500b2a9`

```dockerfile
```

-	Layers:
	-	`sha256:4acd8cc1d0c81e89de4998982e40ef23b66e2e784b4b2789bc740ef3d355f89a`  
		Last Modified: Tue, 21 Apr 2026 23:02:54 GMT  
		Size: 2.6 MB (2551801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e65f29dedbfcce57487ee85776932b320f113f9024691cad76de47e771635cd7`  
		Last Modified: Tue, 21 Apr 2026 23:02:54 GMT  
		Size: 9.4 KB (9421 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:480464661f8d5e5f10b7f427db1582bf993f0a50aa4570532fe1602aa67dd482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85199378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea761f1cd9ee105ccf9ae16833608f140808d0db49dc5dcbb9c5e59af2ed4701`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:04:52 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:04:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:04:52 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131c4c7efdd220d089b0ef93005b54d10c6c1066a05a70c141161a3e69693e5d`  
		Last Modified: Tue, 21 Apr 2026 23:05:07 GMT  
		Size: 57.6 MB (57592835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ef3fbe42f8d7267d9076012ff70491d8e3909893b09b41f73c17ae2a64e8dece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2561053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3c97dc1eda345e6b05959a75ce653a04bd8fd5c14ffdf574a2f3fc6fc0bc54`

```dockerfile
```

-	Layers:
	-	`sha256:10332195a106c16d9311861744508b6d8aed65a7c81358a805338dc8a0cd9a4e`  
		Last Modified: Tue, 21 Apr 2026 23:05:05 GMT  
		Size: 2.6 MB (2551504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3ad57487795f5baf0144e56c2e97f200de4cc3302ef466931698db94d30fee3`  
		Last Modified: Tue, 21 Apr 2026 23:05:05 GMT  
		Size: 9.5 KB (9549 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1ef38f315a6f7378baa83135cba7f5ec366649c218290d6a72eba5a7b78a1785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.3 MB (94342911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3783a521bab90485c164af0ed3f601b8d16ef2e18e4d8dd0b2ce8e64ea460bfd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 10 Apr 2026 09:45:53 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:45:53 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:45:57 GMT
ADD file:95b037c0bc0e563e4cc21cb68d052a809b9c0f9ecf9d5ba02ea25010cde68ae5 in / 
# Fri, 10 Apr 2026 09:45:58 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:11:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-26-jre=26.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:11:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-26
# Tue, 21 Apr 2026 23:11:13 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:1e932ba5ea8593874f43043c4d572f8923097c83173dbf1607f236aa01f353ac`  
		Last Modified: Fri, 10 Apr 2026 11:01:13 GMT  
		Size: 34.6 MB (34648398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d034f9485994880c927576b407d386870629265846371c668ce350e8373747f7`  
		Last Modified: Tue, 21 Apr 2026 23:11:45 GMT  
		Size: 59.7 MB (59694513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:747f4239f4d0f1fc717c941b3d53b24924949a8d99fce379373eb95e1da46fd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2560192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94459e0d34dd02c972bf9da032800054cac3d6f8207e6f5eed320f5513fd5c30`

```dockerfile
```

-	Layers:
	-	`sha256:0671f72da7cc2a6a55132cc6ef090ce10f2c13a519446207f0bc125506c175c2`  
		Last Modified: Tue, 21 Apr 2026 23:11:43 GMT  
		Size: 2.6 MB (2550715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed6b3b2edd80cca3c8e39cbaad568d407376a799dd4538a2b844bc328f4a9dd0`  
		Last Modified: Tue, 21 Apr 2026 23:11:43 GMT  
		Size: 9.5 KB (9477 bytes)  
		MIME: application/vnd.in-toto+json
