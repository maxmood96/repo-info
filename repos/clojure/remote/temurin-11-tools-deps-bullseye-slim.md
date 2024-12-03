## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:44c9b35ecd3edbed14b17417b52e34607c327fcde7bda6708ef79c1050275933
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6c13fb4f297c9360c23c052af8b10121798e0babffcaf278b453901f855bf91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234611003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25660139c55444c81cd7b28e87b8c8ca5d9e028672f7e0392242975902b4e052`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c2c9542d83778e902bdbe34ec8e5bca515a9789b979131ed96c36a4ebfa8ba`  
		Last Modified: Tue, 03 Dec 2024 03:19:43 GMT  
		Size: 145.6 MB (145601457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3d01a9047726f3765e75a257c777ff8b1e072f0675c222936ad830f49558f3`  
		Last Modified: Tue, 03 Dec 2024 03:19:42 GMT  
		Size: 58.8 MB (58756257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32e0413525753ce7908331a6b0568e6df4727f7e61fb7a3f77b4be87d9e79fd`  
		Last Modified: Tue, 03 Dec 2024 03:19:41 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fcf47ea5e4aa8c9361f339cd8caf789eb7c4b2e7da4f2dde2640bba0331f8bd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5158030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dccde571549d525177668f88b29a9ec746ed57146710c657fe8bdb8782ac1b0`

```dockerfile
```

-	Layers:
	-	`sha256:abc9d652c35572326ce7be40ddb363c37934e8bfeefd179c59077b5108dd7ea4`  
		Last Modified: Tue, 03 Dec 2024 03:19:41 GMT  
		Size: 5.1 MB (5143720 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4652e28ea9a77bcb0064061d905516b37e00efa4379184d9689a06101dc90fa0`  
		Last Modified: Tue, 03 Dec 2024 03:19:41 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fce7f5be215d2bc854f13f530dfa6849b377353c362302fac0a98667f1b64800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (230014897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea04b3e656d706dda027c3fa3af9a61874a28a63eae3eab3ede3a3029efdf467`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5dff04b2bf13f7daa9b187569e3dac438596fb37c4f93fe7d65747f4fe8d7b`  
		Last Modified: Tue, 03 Dec 2024 14:04:51 GMT  
		Size: 142.4 MB (142389020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784cef2ecb3d0caffcc594281fd2cb30cb5d16abfa913be8ce35c6ff6a106f50`  
		Last Modified: Tue, 03 Dec 2024 16:14:55 GMT  
		Size: 58.9 MB (58880311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b39d8110de115489cfff712b00eea384021eccf1b1eed9224206514e2736c6`  
		Last Modified: Tue, 03 Dec 2024 16:14:52 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0c3785b359b46151635ea27b8338e3eedab35473189c462f67e5a26883ee138b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5164503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:091b2de8d0edfe597e48dd9b3aa9921eff086b891469f359492bc87ee96785d8`

```dockerfile
```

-	Layers:
	-	`sha256:51d291d6af6d070acf6d4770d97a8e823ef8ab75c7453ed086638d6fda1ba034`  
		Last Modified: Tue, 03 Dec 2024 16:14:52 GMT  
		Size: 5.2 MB (5150076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fffb6990a2a5d072a69e90872bbb6808b56951ede34d98427138376b222c0a9`  
		Last Modified: Tue, 03 Dec 2024 16:14:52 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json
