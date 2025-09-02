## `clojure:temurin-8-trixie`

```console
$ docker pull clojure@sha256:da3d0f96ce3126de9f6c023b72931f061ef88b882147294cb69617fc813fea07
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
$ docker pull clojure@sha256:460a0b5a61b4431bbdd8f09646f3985b44a4ca4c94013d12365ec1bc86a51ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.5 MB (189543288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:850a581e4c50df86173285fa3c0c948e67c77b531e3a14ba4a9823addf0525a8`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
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
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860cab4fcfa3c5cee9dae6da49ad15b6685c63b0ce78f1f836b2ad7b529a5658`  
		Last Modified: Tue, 02 Sep 2025 00:16:54 GMT  
		Size: 54.7 MB (54731307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e334a779e19a052553cfb45bf7552bd42b5a853d4b9c51653dc947763ce47c`  
		Last Modified: Tue, 02 Sep 2025 00:16:55 GMT  
		Size: 85.5 MB (85533056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:930823bf83852285d474156d3157c9f5b8c3aa45f7c3388fbf8e423379464c22`  
		Last Modified: Tue, 02 Sep 2025 02:31:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:96be5be1400a08b802ba5d6bc645bf8d1fd7095a8676fb6d75485d6a4cf6d81f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7598044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a68522f37672a38b556342b83580e82447ea1f878f4ebc49b1c2607d89c131`

```dockerfile
```

-	Layers:
	-	`sha256:b4184967bec496c90076c2dae3416dc3edb23efd2ea72b0ad8a35bb41282bc46`  
		Last Modified: Tue, 02 Sep 2025 03:46:45 GMT  
		Size: 7.6 MB (7583831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5fe64007eaacbfbf35a49373891013f459e96f5e4268e54868098d8e9f399eb`  
		Last Modified: Tue, 02 Sep 2025 03:46:46 GMT  
		Size: 14.2 KB (14213 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4a8bfc298f3052f4f3677001dc3b489f508d641f5909e741988787f53bd34769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188834539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e02437430bcb278d1d31a7e151b0f713a5ab375fcd9fdbddf3ce80ec7931c4`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
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
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9755a39d9db0bb27ba10844498ce216fde72dbbb91279b72ffe90079f384cb`  
		Last Modified: Tue, 02 Sep 2025 07:37:58 GMT  
		Size: 53.8 MB (53835608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ff7bc6f1fc51b8713290001cd689e6cdf8202ac7a3d4521b21af7ad167acb00`  
		Last Modified: Tue, 02 Sep 2025 07:43:52 GMT  
		Size: 85.4 MB (85356680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de2b8681f2327747a175c1bb0fb21a69fc5bba76dcaaf493cf0a8fac5d39c7c`  
		Last Modified: Tue, 02 Sep 2025 07:43:46 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f46c94796c78691413657177395135530fe1ee67dfe4f6237851eb926235a5e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7605890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470dfaa34f461a574f28b5d463bfb7218d4112cb8cc6ad16d2cedf9bfc5cd80a`

```dockerfile
```

-	Layers:
	-	`sha256:4598f2a23ad5be8113883945152651eb58ce6ce71b9da46ad604648d39ae6b09`  
		Last Modified: Tue, 02 Sep 2025 09:46:08 GMT  
		Size: 7.6 MB (7591559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2eef5af7fddabe9aad201d9579403e609e04c73043f181f36bb20734e54ce9f0`  
		Last Modified: Tue, 02 Sep 2025 09:46:09 GMT  
		Size: 14.3 KB (14331 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:99499dee0e73c060164227cb5f51c6f28afcb54d005731b320ee5130e15fa0d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196211903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12585a4141913ba8de6b723168a18e18daf105ca83ff95ec8d4ec92390b30048`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
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
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f01c993c06deaff5be3f128a6eedd6211cc9a4b4a26e7abcdb0e1f30941309d`  
		Last Modified: Tue, 02 Sep 2025 07:56:26 GMT  
		Size: 52.2 MB (52165399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c7f7e8d4b188896ddcd59370b1b23674ef278c88a47f1af41b0adfc997f28a`  
		Last Modified: Tue, 02 Sep 2025 08:07:07 GMT  
		Size: 90.9 MB (90942472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22d35d52538f8cc57b2b6468e610fc7908a6b894d5cd4da0a8e73281f1cdc34`  
		Last Modified: Tue, 02 Sep 2025 08:06:56 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b4421bcc5dd9ddf78a07fc69c09e9604f64edcbb18080c7a24cc55a0a1580928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7603104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0095610d528f8d1a1e72a991b52afebe7c5e6f2f7bef60f4a054a264cb7bf8d`

```dockerfile
```

-	Layers:
	-	`sha256:ea57fe7109f1d1682ae97e07d2fee2bdad1bf98122a99c41ee85de6e4009ca9e`  
		Last Modified: Tue, 02 Sep 2025 09:46:15 GMT  
		Size: 7.6 MB (7588843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce33efef6f93a83391ab86502871ffcd67d5846259580da5549979285e8857f3`  
		Last Modified: Tue, 02 Sep 2025 09:46:16 GMT  
		Size: 14.3 KB (14261 bytes)  
		MIME: application/vnd.in-toto+json
