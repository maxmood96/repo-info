## `clojure:temurin-11-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:d95d91a61a60d80d9a471eba44ee6af90010d7bd8e96e09d0d0ea6831f07eaf6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:55f7f957aafecb4c0b70b8767d94fe8dd6268d007211bc737494fa1afcf23007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275572155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c464a035bbdbcdb065962347f85d5b0c61495b4bbed8558d9e5571a7e3d3c8`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad12865678f4a8dff5371ef93742806d2e3b19c13b44777d1e6fa5d0c6cf80e5`  
		Last Modified: Tue, 02 Jul 2024 03:02:51 GMT  
		Size: 145.5 MB (145505213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6d8f2deb391bcab1b3ae6d3092674d7ae1f5561c146754041dbd16313a1b95`  
		Last Modified: Tue, 02 Jul 2024 03:02:51 GMT  
		Size: 80.5 MB (80512232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0da4dba83ef74f1d64510e7256fd29b9a74cca9a2889295bc39601db2d95ef`  
		Last Modified: Tue, 02 Jul 2024 03:02:50 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e6e36e09cd0a6b5fdc9c487b8cc5ed6cfc2d50566f7d7cdcec4cab6c6f9d8235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6973825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f6031f7f65aa9265f6beaad05ed98ba8089f6317297e29df67e8f0eaf7b91e`

```dockerfile
```

-	Layers:
	-	`sha256:553742b9024f64840862908f2dc3110c4d6dd654ecc451f7e06da0b7edfeb2e8`  
		Last Modified: Tue, 02 Jul 2024 03:02:50 GMT  
		Size: 7.0 MB (6959961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:617d978ec46c4c4a2522a4cd59e06fb1023e09970594dc3e7d7b59f0d6e51ac4`  
		Last Modified: Tue, 02 Jul 2024 03:02:50 GMT  
		Size: 13.9 KB (13864 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1e453a0f11c540c82601cb4cd8af564dfe1ae6c907c72495bddfb192b9eb2ada
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (271961867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea3c3d8831f0004ced58783ea22b2e4e073d324c63c02f609f6d1281ee79721`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:cfc8f76c8181d3ae6dda16ae894b184c69dbba114d446426e466126fe0ae62e5 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1e60a453843e00d6f3d4242dbd696365f0894e3ca2f02f4ce1ab098d7ff7907f`  
		Last Modified: Thu, 13 Jun 2024 00:42:50 GMT  
		Size: 49.6 MB (49613402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c994443e04e21bb1306b98beb1d8092f88115cd46256bc1fab8093e67ac36682`  
		Last Modified: Thu, 13 Jun 2024 11:28:18 GMT  
		Size: 142.3 MB (142304076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58a010ce25cca5e1831f9847741d4c4c914229a4ada2c8494ca1f24b23c44a2`  
		Last Modified: Thu, 13 Jun 2024 11:31:39 GMT  
		Size: 80.0 MB (80043741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b593bf413a7e65204bc9d7679e1e54e5469968219a5044c9fda12ea20764a31`  
		Last Modified: Thu, 13 Jun 2024 11:31:36 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e428de6bd507596ea3af40119a43b881cd66b3bf10bca097aabbec9d7fd9593b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6981453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5c4ebbf19797ea9411e881bf947b3e1f173a3a9a40315382d1471663d7ce9b5`

```dockerfile
```

-	Layers:
	-	`sha256:44c2fe527cbab997cf463a30fd544499b1372994bf712dc2d5e4bf2649aabdae`  
		Last Modified: Thu, 13 Jun 2024 11:31:37 GMT  
		Size: 7.0 MB (6967053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68783ecca6a31734472c4dafcee920de464e2401bf77a327aed2ebe249baa2bc`  
		Last Modified: Thu, 13 Jun 2024 11:31:36 GMT  
		Size: 14.4 KB (14400 bytes)  
		MIME: application/vnd.in-toto+json
