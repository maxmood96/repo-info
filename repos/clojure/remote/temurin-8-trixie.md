## `clojure:temurin-8-trixie`

```console
$ docker pull clojure@sha256:d67f3db5e4724427387de461f5cf8a8155b832046121b4d5a4a7f89d93b78e7e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:fabe359cd643939e1571cbd60ab414c91f09e0ead59742a3ea8731661759dbb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.4 MB (189445827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e154adc001506bc2a104f26593f75d8010a59579399558a13312946292840e9f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a2310ddb3c240b2cc693b69cd20f833f5a698083d6b2721eb3ac0723c23407`  
		Last Modified: Mon, 18 Aug 2025 16:53:09 GMT  
		Size: 54.7 MB (54731354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b7915d6d86e31b9913cdf5374daab863604721fa00514e08d44a414c87b501`  
		Last Modified: Mon, 18 Aug 2025 17:08:32 GMT  
		Size: 85.4 MB (85435549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447e37d5c090562bade048f22bd2e2d5dc3eed644a73c0ef84af0b65cad33eb4`  
		Last Modified: Mon, 18 Aug 2025 17:08:33 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c067ddf95a5bec150826cc07bbc4a2418090bd96fa15d892f8f500e1d61c8405
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7598044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7049a9e43d082944a3e11c654305ee1b228c1e994bdcdb5591a6239386eaa1`

```dockerfile
```

-	Layers:
	-	`sha256:4c3fc5eb800759d52795aac9f8ab707dc9d975ba9e322defd9294e2b3b20d255`  
		Last Modified: Mon, 18 Aug 2025 18:45:45 GMT  
		Size: 7.6 MB (7583831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65996ab0b96a02b31e873fcd473ff10d0ddcd70e86ea5f95fd3bf2da544d3f44`  
		Last Modified: Mon, 18 Aug 2025 18:45:46 GMT  
		Size: 14.2 KB (14213 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1fac1ad3b9432aed84d71a85c763e7fe8b7fd1b9feaffb08f713147bfed8b7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 MB (188734174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8e1821c364e83deb6f20e5899a835d5e9477c9facc3df51ac464004a1a1f44`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d601e9520efa7df3d63d77147625a058590324ed389fc928416c360b90f26b5`  
		Last Modified: Mon, 18 Aug 2025 16:58:11 GMT  
		Size: 53.8 MB (53835608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31856e27f2e82502ede033c0d44af7c88562795d858df90276f827944646aac`  
		Last Modified: Mon, 18 Aug 2025 16:58:21 GMT  
		Size: 85.3 MB (85256318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe512b75f55274cc5079a9d17e13374304d5a3a0b247818a7eeeb6d09bd2d933`  
		Last Modified: Mon, 18 Aug 2025 16:58:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0e9cd70f6028cbcc9c72e24c0fd2706ee1762bf932e571f42421a7fbdf4d25ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7605890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a4caaeea1c73185f095a569e95a758ba06d6a19e1a0e843a3ca3d029405e09`

```dockerfile
```

-	Layers:
	-	`sha256:e9f15ec0cfe6de442a37bb13f977c8aae319deaa58cae86de7527d640d145c7d`  
		Last Modified: Mon, 18 Aug 2025 18:45:53 GMT  
		Size: 7.6 MB (7591559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a022a195260c6c5aac495bba4d96b95cbbbdc5f0203a58ebf7e7b29fe0f0c7f1`  
		Last Modified: Mon, 18 Aug 2025 18:45:54 GMT  
		Size: 14.3 KB (14331 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:2965b58f63857ba1c865a2930fb862c3925c66bd884e9ead0d3666cb865b2143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 MB (196110108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1b8980c18435643217d39a93de94b8381526763bf02d752cc77f439da5caa3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959807e042cfcaa6a6f91ac803622b4131aea7366490c83817cc1b36e2a904a8`  
		Last Modified: Mon, 18 Aug 2025 17:05:01 GMT  
		Size: 52.2 MB (52165401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee9ac3599b8eb7f01b1f785134b4c933ae746aabba8ed0e4a610c239a68ca516`  
		Last Modified: Mon, 18 Aug 2025 17:05:08 GMT  
		Size: 90.8 MB (90840677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7340a18266ae96f1ed864815a7ddb9666739cb9c0b2304e029b69e1d9b8d39c9`  
		Last Modified: Mon, 18 Aug 2025 17:04:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a143f4d8a326c37c2ecf43895dfa92693069bf48a84366babde1320a07694bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7603104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1478dfae12cd3f86b198f88c6f1ce04398ea87bee1ca4675569af9f5770c1356`

```dockerfile
```

-	Layers:
	-	`sha256:30db015f57a0741c20dc8e23f580029838446714a85690cb1998b2f3a79076d6`  
		Last Modified: Mon, 18 Aug 2025 18:46:00 GMT  
		Size: 7.6 MB (7588843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9bde5de3aae5d0384891a522a0273cfa9dd0978e02ce64c71b35907c2bcf530`  
		Last Modified: Mon, 18 Aug 2025 18:46:01 GMT  
		Size: 14.3 KB (14261 bytes)  
		MIME: application/vnd.in-toto+json
