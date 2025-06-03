## `sapmachine:24-jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:e13768cfae3ac55a1cc5f4526c858b090d2718253c71db76f7443f2ad41224d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:24-jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:8c905afbd0d0beeaf7fe8e52bac6375971cc5bdc9742be091690f18c1e46966e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.6 MB (96601147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae643ff0cc3109d37eaf838732ad45aefc1f713fb17040d792e8602ca7ffb09`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Thu, 29 May 2025 06:11:31 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e697426247ba011272d67d96d0947a538ab47c782ef764503fc96fb100a26ab`  
		Last Modified: Tue, 03 Jun 2025 04:17:35 GMT  
		Size: 66.9 MB (66885810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c57b6a0a92e25b0cca9d6070084a265dfddf0d9304584b5cc737426a33073285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d845fd180e2ca455f8286a9d9365f4ff02db9211ba7dd38256ab829682de6957`

```dockerfile
```

-	Layers:
	-	`sha256:ba730196f9f7de1157577f2b3d7e54e7493eb0d2779d6029daa595bef02b2ecb`  
		Last Modified: Tue, 03 Jun 2025 04:17:34 GMT  
		Size: 2.2 MB (2179260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cacad6db05f0bb26346c35e794c8d51bee578a6deff9251b01b0488a13403aa`  
		Last Modified: Tue, 03 Jun 2025 04:17:34 GMT  
		Size: 10.6 KB (10627 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:325786978841eb4ff81621f5313ce3884e399b311c734d73d3a03776763e4095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94772826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b71b482f159098b1af2a607ac22e54b712fa00f68e6e1d2b46f3dea4f19ae9`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:6eb9adae2c7e3a73446b74d4e61e58d6e1d0db6c07cc49612eb0b9f38fefef15 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:69c262fc30fc134b6d373dee8db695319c41d8b9489deb0f682565473bf29748`  
		Last Modified: Thu, 29 May 2025 06:11:37 GMT  
		Size: 28.9 MB (28851899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca6f709779d78e1ccc12e7c895d70bed8e67008ce2bcebd96ec1a6e0de33c85`  
		Last Modified: Tue, 03 Jun 2025 05:54:20 GMT  
		Size: 65.9 MB (65920927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2829d9c9e51f30ab6ea1227ebb4b76fbee68b13221a05a27eeb8a37de2db79bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca8fe1df7fac1684b7f614389157b28018fda396468b11195952adfe82ff9c12`

```dockerfile
```

-	Layers:
	-	`sha256:b2e2fd04d46e448b41e2c747857e4fd54b27d6004ef244b741c92df3de52d590`  
		Last Modified: Tue, 03 Jun 2025 05:54:18 GMT  
		Size: 2.2 MB (2179776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:636adc684e87cfd1c63cc325c5ebbb6b76f7e37edb4a4d5ce5615b71ffcfc3a5`  
		Last Modified: Tue, 03 Jun 2025 05:54:17 GMT  
		Size: 10.8 KB (10791 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:24-jre-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:659ab0ea9b41a299b3b5095b90a72203ba90dd603dceb213aa0750ab708a9023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102389695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2441681e238a539530e278db1b661f70b756cd4875983d520ff8b5065fbf3759`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:47 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:47 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:47 GMT
ADD file:5b5c63079c35f826dfba60892de9b0b4108ed6547a12101193a481b991b1add9 in / 
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:47 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-24-jre-headless=24.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-24
# Wed, 16 Apr 2025 10:34:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9f6c4197b204ad8fd01f03e4a049c781a2075478303fbfa660f581b019365dab`  
		Last Modified: Thu, 29 May 2025 06:11:52 GMT  
		Size: 34.3 MB (34325210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23522ab9bd7d9b8b3bc8137bf4cc100f01e729216ec3c995aaa959afff5b136a`  
		Last Modified: Tue, 03 Jun 2025 05:47:54 GMT  
		Size: 68.1 MB (68064485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:24-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5cd564d4ff3060e51bc6969b819589e0b5c09a7e8e2776d2c14f5194a24e2e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2193351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4ff604ab1deda983aa9c18cf7ecb25e239ce0b250c7d820eefa0db24162b5c`

```dockerfile
```

-	Layers:
	-	`sha256:578aaa1648e8002659a1186eb013745fb185ed69e73a981f5217a7a297eada82`  
		Last Modified: Tue, 03 Jun 2025 05:47:52 GMT  
		Size: 2.2 MB (2182652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f75586ffaf0ab9fafedb4b8e3246ec13fe0d6c148c6c7d0e1b4b7b52d3fb8257`  
		Last Modified: Tue, 03 Jun 2025 05:47:51 GMT  
		Size: 10.7 KB (10699 bytes)  
		MIME: application/vnd.in-toto+json
