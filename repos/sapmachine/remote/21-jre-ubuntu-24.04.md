## `sapmachine:21-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:b3823498315672ead7e307559705904dcd51230c43b37150e359023691e2fdf1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:01fc791c894566b111d8fcf99c506f9fc7d390edcdc6c9b9bd8603059ef10020
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92331278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f1ddecc0bad289a8be99c64338db3fdf4b0504d7753f5921fd8e5786475cbfa`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:32 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 11 Aug 2025 06:09:32 GMT
ADD file:d9cb8116905a82675c3c2cbb4782e50ef8cacfc16be3654bc070281a3c8ce646 in / 
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:a1a21c96bc16121569dd937bcd1c745a5081629b3b08a664446602ded91e10a4`  
		Last Modified: Tue, 30 Sep 2025 16:57:55 GMT  
		Size: 29.7 MB (29723011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d8f5a643f44d7cc591e25f38403398962ed493e31e6c7bd4414a814d83b89b`  
		Last Modified: Thu, 02 Oct 2025 05:19:38 GMT  
		Size: 62.6 MB (62608267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:de1877175d40b52e9e52e49336275758fb03f54312dc45478895ff81b257782d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2528712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71cecb11bb50090008fa1aca065b774f1adf2ff5ea70da77fd5d5a8d26efa8ad`

```dockerfile
```

-	Layers:
	-	`sha256:6f075f0ab210bca9fb659e10e446f4e2ec14843be7f1178b1181da3ee0a209c3`  
		Last Modified: Thu, 02 Oct 2025 09:09:46 GMT  
		Size: 2.5 MB (2518632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aebc7617c0ee57b8494d4124892d94f4331de9cc7a17d606ddc03ecfe0a13bbf`  
		Last Modified: Thu, 02 Oct 2025 09:09:47 GMT  
		Size: 10.1 KB (10080 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:e568ac4f72d53ec6a09a723c8236753740497b10104c5d78762f16dc7151b256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90471263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e78da114991ec5bc92e5a001fff307c34cdb70b74b1d899a626f2270bd7c08c5`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:32 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 11 Aug 2025 06:09:32 GMT
ADD file:2b1a3adb91c564e3fe655be94477504bbc81d767317b3181efd5cd6ae287b26f in / 
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7bdf644cff2e9be580c17c3db8d5fc564ad093513bf0fbebebc392c17fa925e5`  
		Last Modified: Tue, 30 Sep 2025 17:07:37 GMT  
		Size: 28.9 MB (28861575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b406a6532f571357eec77cfd1847b4513eafe91cd4a4eee6fcf7d16c5446f0`  
		Last Modified: Thu, 02 Oct 2025 01:34:19 GMT  
		Size: 61.6 MB (61609688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8d91ef2067f5f9a280f9aaf788b74f5d32d780d690be4b6288d4149f77d4da81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2529380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff8458e9c21dd3c9cfa9a3a82911204d54615d6735c33836b71d75a7b65bc45`

```dockerfile
```

-	Layers:
	-	`sha256:eab06de3ee60d4f97683ddc101cb1ca6f8d8ad0054d82d5c6fe853569f0c41ba`  
		Last Modified: Thu, 02 Oct 2025 03:08:09 GMT  
		Size: 2.5 MB (2519148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84ddcb856c4fe97e7b04a597c84c08981bf0ade7ad99e92193e7929d16c88d8d`  
		Last Modified: Thu, 02 Oct 2025 03:08:10 GMT  
		Size: 10.2 KB (10232 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1d30cfe5c372bab5f51c0062c10f78f5fff9ee5e030e2c5cd3876a75c8e0f63e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98366543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73080c227757113ad30808c0a1df818469dabbef9e550255502a4cfe18f9e7f3`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:32 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:32 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 11 Aug 2025 06:09:32 GMT
ADD file:c654664ccaf1c501c787c924fddcfab7f9cdc324325d45748f97ee6d5ad63cec in / 
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:32 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 11 Aug 2025 06:09:32 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:15a6b79c4fd2f3417787ba4c0a8161183cf898454880102c719eb0c91671c218`  
		Last Modified: Tue, 30 Sep 2025 17:28:16 GMT  
		Size: 34.3 MB (34303547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b663f62421fe3d2c3be3788263f8d374989a69723a0ce541006580d91d2d7032`  
		Last Modified: Thu, 02 Oct 2025 04:31:34 GMT  
		Size: 64.1 MB (64062996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ea9494013bf91f4fdbb9465ce3eee4d110bea84c86aa4cce828ced1000df8c38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2526860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:853ac2d50afcfe4550c6cadf8ac65ae4e0925363eafd9e1ee44aff9369c927ef`

```dockerfile
```

-	Layers:
	-	`sha256:930e8f8a88d07eb228ed61e96989c5ad9824244251f19f45e8e78bd1e4e0f3f6`  
		Last Modified: Thu, 02 Oct 2025 06:08:15 GMT  
		Size: 2.5 MB (2516713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a1ff61885a33210bae106d14b8ff13b7572440c263f99d187a73799f9705ba1`  
		Last Modified: Thu, 02 Oct 2025 06:08:16 GMT  
		Size: 10.1 KB (10147 bytes)  
		MIME: application/vnd.in-toto+json
