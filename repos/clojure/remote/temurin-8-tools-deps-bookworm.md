## `clojure:temurin-8-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:5eec48ff80157a3b332e6d18cf29038c92a50dcdd7e86d149f93742b650550f2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:ee1a2ea7a44bb91543e5a2287de2b3632bd4c565fd2ab6d29d1dcf192fad7955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234095725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8e253d63dcc497b46e24843f87157ed11ea07c0b1803b9757b5c634bbc4323b`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
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
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d267253c9a938843266237fd5a9d4e8aedf113b06f077bfdbc031d0599ec033c`  
		Last Modified: Sat, 19 Oct 2024 02:55:25 GMT  
		Size: 103.6 MB (103611910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9cfad3843ac906dbd9232599410d9023047356bc786ed09e286885136ba1e6`  
		Last Modified: Sat, 19 Oct 2024 02:55:24 GMT  
		Size: 80.9 MB (80928149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97bdbf179dd046a6d79f0806244f87cd6176b306f83dcf669fd793fb570da3d`  
		Last Modified: Sat, 19 Oct 2024 02:55:21 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:10135471d08c601e53c0fc8b58fc2d5b88f7db8c630008ad176a2088eb5975ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7318617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40fbf7d1e6b2ba2c0fd7e7a9d5b1e84d87e209f9756c895c46639ef45ee1359e`

```dockerfile
```

-	Layers:
	-	`sha256:f78a9622bebb6de99bbfb7b32dfa62ba72d80be246b22694d09899c0e5806988`  
		Last Modified: Sat, 19 Oct 2024 02:55:22 GMT  
		Size: 7.3 MB (7304557 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39de99e6812312247f780cfe349104f2558cf0f45a995681de1ad7f18fd67822`  
		Last Modified: Sat, 19 Oct 2024 02:55:21 GMT  
		Size: 14.1 KB (14060 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9e69681b390c27fcce7b273e02ee2dfadb4553b6234074fb0c384185fe747206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233105117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0917ef4f1b67097a84cb2475d8ecaa720924f7d7285c9c5812f2ac9e02942954`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9cb4bfb17e76b2be909686d0dad899be2eb91d7bcdbfbb6e70051a27952293`  
		Last Modified: Thu, 17 Oct 2024 07:55:37 GMT  
		Size: 102.7 MB (102729275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4966bfa4e3d17d761336a0961a8e905c955b2d2d40e643f116c3a81ca22fe96`  
		Last Modified: Thu, 17 Oct 2024 07:59:39 GMT  
		Size: 80.8 MB (80790220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6bf02ba41552aecf84ce0da7e9574ae404efdc5d278ceeabedfcb6eecd2b664`  
		Last Modified: Thu, 17 Oct 2024 07:59:36 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5c42de90bcd045cfae680c64b53e06837553cc4545900b7c6d18cd8a678891de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7299275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cee37f5c68b3f5d7db39a5d3b21fa94f9b4b80f9e450202809e8e02748e893e3`

```dockerfile
```

-	Layers:
	-	`sha256:10c5d09895a173cc9df4b0cd3245333317006acc4a1f935cd435e32928da76d8`  
		Last Modified: Thu, 17 Oct 2024 07:59:37 GMT  
		Size: 7.3 MB (7285279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0692990bc11619023cd322ccf3328347c7bb25f32a91e30505a7af83529e535d`  
		Last Modified: Thu, 17 Oct 2024 07:59:36 GMT  
		Size: 14.0 KB (13996 bytes)  
		MIME: application/vnd.in-toto+json
