## `clojure:temurin-17-tools-deps-1.12.1.1543-bookworm`

```console
$ docker pull clojure@sha256:2850cc6a8215615b47c640f7c390d71a8a26d6e9ed5ef08ee6ad3a3560cc933e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.1.1543-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:6a5bcb96cd97d867a5ad8eff3b6c34a4fd443a8d3fc5db6b5305939deb6e30dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.1 MB (274118360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfd231053155be16a128d62f4a2a8eac77600a649ace2b477d90d85e1dd6439`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ef33633ffd525941c8efc29c40275178655b3b7c603eb713ffdaed6a1c736c`  
		Last Modified: Wed, 04 Jun 2025 06:05:54 GMT  
		Size: 144.6 MB (144635013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6961f7973c7f0ce95bda892026f1464b5d34a6b8ba29d4969a435472da9c23b`  
		Last Modified: Tue, 03 Jun 2025 18:24:36 GMT  
		Size: 81.0 MB (80994065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8ce6c211a66fd8b91da59a45364db84bf248f1986504148fdd6e2ecb1d5bd7`  
		Last Modified: Tue, 03 Jun 2025 18:24:28 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e336250278adc4e0f7c8a13b8e1368ef0a84cbba331da56eaed867d4d3712f`  
		Last Modified: Tue, 03 Jun 2025 18:24:29 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1543-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9d87ac3d7a814abca6d49d56f22f62df41c5e6a3f51a1ab7f6f157377293e5c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7234343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d03c36319430bc28ee879208e3c8a0db1df4e517fa4ae1d38431f6b8d8d08277`

```dockerfile
```

-	Layers:
	-	`sha256:aba717515a96b0a50f015bf73a376e4f8681c407a3bc43cb85c1a53dd268af97`  
		Last Modified: Tue, 03 Jun 2025 21:37:16 GMT  
		Size: 7.2 MB (7218522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f469f8ac379d976d30eb49c211cd53ae4dde836b855a7f30e85ee9f59c688079`  
		Last Modified: Tue, 03 Jun 2025 21:37:17 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1543-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aff74d7929cf21066978b44c7dae231d26a4346b940006d54a8daa3c7499745d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.7 MB (272689393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:749618a24047a2f89f8a5f424060c64b41870c1f87eeb2c3b087f23529202528`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d616bd6f18b21e8af2a1fae7e0a03786fe00872c2eb14456c4dc4039bfa80bd4`  
		Last Modified: Tue, 03 Jun 2025 21:49:58 GMT  
		Size: 143.5 MB (143512624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeaed219fd3da97a5d44c7594bf5610a5be94078f797e15be349c1e508fa5451`  
		Last Modified: Tue, 03 Jun 2025 18:39:02 GMT  
		Size: 80.8 MB (80848550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f5b58c50634b083757de76bc8ec8488f2cf345d26f31182170e582658e7929`  
		Last Modified: Tue, 03 Jun 2025 18:38:44 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7066b9a8cea7dc186a8ad6f3061a7f4e7d0998e3f2adf84c50645c8f9821185d`  
		Last Modified: Tue, 03 Jun 2025 18:38:45 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1543-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:226dabe6564021250b4ddcc51b1e97ac68de0539965c8879c13df25aca2b5887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7240224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8538c4d2adca8648b9f44b7ffdd9cb4ee31c8a771508359038991842509cad6`

```dockerfile
```

-	Layers:
	-	`sha256:846d20a3b4468233a76ce68bfad7e7e5a0b80ff6172f3d25ff065c7f6cf47cf9`  
		Last Modified: Tue, 03 Jun 2025 21:37:28 GMT  
		Size: 7.2 MB (7224285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:817128eb86c17163674b65696bcb154e7ddd355b76d06e8a28b0637ab2430bb4`  
		Last Modified: Tue, 03 Jun 2025 21:37:29 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1543-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:418a8480a83618615472af4676438068dbd222c34a141511b1e14a96199f9f9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283426730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f5822efd819b2d81cdfab71ec0893d767769d61f276811e79b6eade9123f019`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5fca0800952ffd845ecae7a757898651fb9b497615be2e0d7662f4d7ff229e`  
		Last Modified: Tue, 03 Jun 2025 08:44:24 GMT  
		Size: 144.3 MB (144280554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca88bbb4b9cafd0033c6e06bd872d90c931a05c39d76038aa4fa555178d92a40`  
		Last Modified: Tue, 03 Jun 2025 18:49:48 GMT  
		Size: 86.8 MB (86813515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57300c92e4084ac5a246eaf76189277780a0f9a6dd097838fb0e508de2217198`  
		Last Modified: Tue, 03 Jun 2025 18:49:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c77a062c5e14ecd5baceee83c7f476a41808fe045d551766395a5de78b1e7ba`  
		Last Modified: Tue, 03 Jun 2025 18:49:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1543-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ffb38621dad16e10f45fa7396c2b625c8dda226b4ac85edf29e2b44a8c28be33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7239595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a92a5af8dfad38fdfd8042d5269486d866965b176e7c696b2b16b79b881e6b`

```dockerfile
```

-	Layers:
	-	`sha256:d9f0724c3021b214a2b7c62160748f7128fd770c691f05be70b827a99d63284c`  
		Last Modified: Tue, 03 Jun 2025 21:37:34 GMT  
		Size: 7.2 MB (7223726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:315964ac794f4530abfdfd9352d8bc6fd9934a34234c25783ad9f0e0dd947fc1`  
		Last Modified: Tue, 03 Jun 2025 21:37:35 GMT  
		Size: 15.9 KB (15869 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.1.1543-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:daaaee7c8ca4edecb9e65b9af3aec1af26567938f1a1de4fe2f88363596566f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261621297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1573810f72bbd768da92fddb7ab33922d71970e6462706c7ccba74c35bd4fc0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Tue, 03 Jun 2025 13:33:39 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f22e4165e784cf5cf4630de4aad9261205dcd457d5c03fd507e8f308626656`  
		Last Modified: Tue, 03 Jun 2025 06:12:24 GMT  
		Size: 134.7 MB (134673548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe9216e9576ba9f96fba2ce3bb82a47ddf44c56adaef0398d0209fa32187f7a`  
		Last Modified: Tue, 03 Jun 2025 18:31:40 GMT  
		Size: 79.8 MB (79802867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd521c64c3c3def1c528a745008c4f312a396051f7dfe93fe6700cc339fa823`  
		Last Modified: Tue, 03 Jun 2025 18:31:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1c5806a8c2dfb137ac8b6d772b1f0a3a5131fc59b570c335d0bc68da4dd456`  
		Last Modified: Tue, 03 Jun 2025 18:31:38 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.1.1543-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d712268a34f5c255d93015836990c07934d0f08d2555bec1394cd9c2de51e764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7228554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbb556484a8ab0a9d63ed16178908082d64acb501d456016ad208dbfdd18ca5b`

```dockerfile
```

-	Layers:
	-	`sha256:4f4df6a2912f0c0ce2f7ff74f363292bd1354d93b712ed2fb53df62f78d65c1b`  
		Last Modified: Tue, 03 Jun 2025 21:37:40 GMT  
		Size: 7.2 MB (7212733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcbcf78c931e8d52cccacbdeb46a22f5136564059d2318a962df58da2f17e493`  
		Last Modified: Tue, 03 Jun 2025 21:37:41 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json
