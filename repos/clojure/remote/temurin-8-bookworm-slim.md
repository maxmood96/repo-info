## `clojure:temurin-8-bookworm-slim`

```console
$ docker pull clojure@sha256:513927fcaffe538a4d35c27c1e2198492072c1a0e2bb3488383271163d010adc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a16caac9d5ee878c4fb241d2d967c8f7472a22a4fefd26ebeac91cc9a95cdc9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.1 MB (153134525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42a9407ad0bdb4bae2dbde779331ad9805a2c173331573135867738c5252e688`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Tue, 12 May 2026 21:45:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:45:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:45:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:45:52 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 12 May 2026 21:45:52 GMT
WORKDIR /tmp
# Tue, 12 May 2026 21:46:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 12 May 2026 21:46:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 12 May 2026 21:46:07 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abe6c05dfb2a3f8b2c259e9928860afd2ac717e55ad99a5ca102639d1bd458e`  
		Last Modified: Tue, 12 May 2026 21:46:23 GMT  
		Size: 55.2 MB (55198701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af979dbbbe309142ceecf2edfa0284c22ff46eb4d3b1bd5de313e53201e3ed8b`  
		Last Modified: Tue, 12 May 2026 21:46:24 GMT  
		Size: 69.7 MB (69698894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a6369283237e5491f260d3b2adb96cd22d804e75e0a88746c5f56de74cc24f`  
		Last Modified: Tue, 12 May 2026 21:46:20 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aeadf802941b79145eec57c1a5ec8a8fca662748b568edbb1e9492ee34d231d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5251556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5591f2d3ac7a65b5b7b46748b3397f7c909e37b7bdf1283315a5d0d3389b402f`

```dockerfile
```

-	Layers:
	-	`sha256:02e3d6b8f6970091a146ade86eb71fecbb65dbb3cc036b71ddfefcaebc397d7f`  
		Last Modified: Tue, 12 May 2026 21:46:21 GMT  
		Size: 5.2 MB (5237154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd7d45270083e54547fabdc41e9e29e28ccf94fc7bf9997ff4ec3f8ecc9c4d7`  
		Last Modified: Tue, 12 May 2026 21:46:20 GMT  
		Size: 14.4 KB (14402 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d2d844b81ec3f1540a8c5240cd6fdbb5dd674e82542716fd6d617780a9875caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.1 MB (152082216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea1233cbd45efb8286d1f47350119b05c0916274e2d9db2b38e3546e45e1da1a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Tue, 12 May 2026 21:45:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:45:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:45:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:45:46 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 12 May 2026 21:45:46 GMT
WORKDIR /tmp
# Tue, 12 May 2026 21:46:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 12 May 2026 21:46:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 12 May 2026 21:46:00 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a624afbabadc81be581e1a1555e39e372a988676eb2e1b4c01e4dcd0a04c8f5a`  
		Last Modified: Tue, 12 May 2026 21:46:17 GMT  
		Size: 54.3 MB (54272958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe3be476924d95f277560aca98ab828bab66b67bf2f970550c6b5a8b1edab5c`  
		Last Modified: Tue, 12 May 2026 21:46:19 GMT  
		Size: 69.7 MB (69692447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0959346b972cd2deecc9652a09bfce64bf52a9e3e7e1e5344747b1c917796313`  
		Last Modified: Tue, 12 May 2026 21:46:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1d933c63916fe5a4d76e9ffad7a625b585a6307fed84433bc5582352a82a1526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5258135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b08875d9cb66294517a58e65bd3767546b4cf4d1d6b947bc7fb7999d0708e23`

```dockerfile
```

-	Layers:
	-	`sha256:02ff587665d65df04dd98d89d6798413d21abf9ea12cb4f92b32354af65bc21f`  
		Last Modified: Tue, 12 May 2026 21:46:15 GMT  
		Size: 5.2 MB (5243615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f695d3a16ac0702b9e7980d45c6cfee13a82748ce14fa2e6f2dcb44cb666ea5`  
		Last Modified: Tue, 12 May 2026 21:46:15 GMT  
		Size: 14.5 KB (14520 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:0f1bf2eda8fe070d14c76fa1ee738d7aef6a7065c2143091396d5fe49a0f9913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160277963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6b7cc9c765f24cd170bb6ea68a5def775b14526234f59e76c914303cc3a5f5`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Tue, 12 May 2026 21:46:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:46:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:46:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:46:26 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 12 May 2026 21:46:26 GMT
WORKDIR /tmp
# Tue, 12 May 2026 21:51:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 12 May 2026 21:51:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 12 May 2026 21:51:13 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57a4137454cc0810d06042c272eb08276000e4b66a91f77145ef48d12c8463a`  
		Last Modified: Tue, 12 May 2026 21:47:32 GMT  
		Size: 52.7 MB (52669152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bde1ecaaf85d1e1fa0ad922be734bfd2566d0b89605feed345f39b79f4eee1f`  
		Last Modified: Tue, 12 May 2026 21:51:51 GMT  
		Size: 75.5 MB (75529711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f15b211cc2d16a9ae7487846c3a2511cd7c3a3e248cce33e2cc3ffe7eb6166`  
		Last Modified: Tue, 12 May 2026 21:51:48 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0d9084fb054cb5d05458a91179213c6c0b672a77664e2b622659eaad454fcf88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5257355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7098aea6a6a74f624c563e80ad58f8cdda05364e8872baadb3dd0d58dc84f7`

```dockerfile
```

-	Layers:
	-	`sha256:f49f799d07e220c3def53c3067a5737f14b21c438b9d6541ff2fe6a12d3c1955`  
		Last Modified: Tue, 12 May 2026 21:51:49 GMT  
		Size: 5.2 MB (5242907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc60869fd63aaa51b2fa3383d4a5dbb54b08036dd48e7ec393113d169d2662bd`  
		Last Modified: Tue, 12 May 2026 21:51:48 GMT  
		Size: 14.4 KB (14448 bytes)  
		MIME: application/vnd.in-toto+json
