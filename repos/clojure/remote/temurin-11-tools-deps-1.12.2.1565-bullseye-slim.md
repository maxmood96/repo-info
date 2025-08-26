## `clojure:temurin-11-tools-deps-1.12.2.1565-bullseye-slim`

```console
$ docker pull clojure@sha256:6f8a7f4cebcfb4482a6b5951dd34f000e3d1891918338da7c8d942ea4a3216c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.2.1565-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:409c8f7843422d413fc5aec304509ae9501591d4a179b2868e4abb5bd2bec315
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235065860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b7950fe5830741b7efcd4e964ecb0ffb2597b2fa033f5703ea74d9378a449cf`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3e41ca17193bcd7630e4dd210602930b1f94464bdd59680bbf6654206f7707b8`  
		Last Modified: Tue, 12 Aug 2025 20:44:40 GMT  
		Size: 30.3 MB (30256118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061433f9fff2290315a6a52e528a4a844de06ed0788b14a1bb4b76d19d1a058a`  
		Last Modified: Tue, 26 Aug 2025 18:46:23 GMT  
		Size: 145.7 MB (145658140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91d5a8653d97019cf31ed25fe0b6e6910efb4746f85a926a1e1be7408faffbe`  
		Last Modified: Tue, 26 Aug 2025 17:27:58 GMT  
		Size: 59.2 MB (59150955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bdda351d341a7494aed80eddddc5230c3ef7dc7ca83e213013b87222a6359e`  
		Last Modified: Tue, 26 Aug 2025 17:27:52 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:083c8b8f1594803114b5653b6099f8d0656213765bce322844aac053df82c014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5342517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a0721a76b58fd72265d9b4eca057d696ab13c69b1a2806204a58f259383c9a`

```dockerfile
```

-	Layers:
	-	`sha256:23c593162d1516f5cbecc22698ff3a9b5223d554d91adbf71ac32a09de1da47b`  
		Last Modified: Tue, 26 Aug 2025 18:35:21 GMT  
		Size: 5.3 MB (5328208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ed7cc9e6a1444063e45579e61b29bb46b776c23df955da8effc82e23d355281`  
		Last Modified: Tue, 26 Aug 2025 18:35:23 GMT  
		Size: 14.3 KB (14309 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.2.1565-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5dfab2bbf802dfdb71017c854303119c4bf3957bc057ceee62ce2b2f1487bce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.5 MB (230494471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:605447ba18af04428876b8747d74117f327330cd822f198f9481b2239020cdb7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b99ef417bc3eb3946e7b3162f6c19dbca1039f3b4124deb116c3a0ab763e65ad`  
		Last Modified: Tue, 12 Aug 2025 22:33:30 GMT  
		Size: 28.8 MB (28750491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd3d476a7a6112e6c89c0b42631d80c8765bc27fb674cdd8928b9d51b6789623`  
		Last Modified: Mon, 18 Aug 2025 17:07:47 GMT  
		Size: 142.5 MB (142460572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5fe058dbfe69d7907eab2f72326ff68569b4c8d58ed51b74634ad747c6da28`  
		Last Modified: Tue, 26 Aug 2025 17:37:23 GMT  
		Size: 59.3 MB (59282761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba0c85ff1ad06bf98e4a192057c2f81a217f58e9e8f787a4bceb939a3ecc559`  
		Last Modified: Tue, 26 Aug 2025 17:37:19 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.2.1565-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ff656c494953f4b02bc9fcd5c7610e8ee9f32e2da4bdaecb4a2639a2813a3c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5348986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e6a64b5464b10bd3314a5d1ba2e06bccb06bc870e6753ee5e9eacc80d8cb984`

```dockerfile
```

-	Layers:
	-	`sha256:aa2fc8b52f377e92fc077d99814020946b13c578cdf013b5095130aff920fd19`  
		Last Modified: Tue, 26 Aug 2025 18:35:28 GMT  
		Size: 5.3 MB (5334558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d48d0a2aba116b214abcafc41183e8bc1c1565b2474566f2ac238185e32a642`  
		Last Modified: Tue, 26 Aug 2025 18:35:30 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
