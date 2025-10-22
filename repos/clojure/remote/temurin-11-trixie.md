## `clojure:temurin-11-trixie`

```console
$ docker pull clojure@sha256:5365101b0519a43e8d319e19a23e31845817a4ab27a5af5b966446914231fda8
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

### `clojure:temurin-11-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:faf0ca09a18387163f4a817c5181a63649b1690e403f429bf86508e680ec31b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280487165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d467ed5152c19415a209ed9b4c5d50e70527d616e635ab32bc0d0d6ca8605f9`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:795dbedde24d2c72dafd2b71fe36643552e56859c0e29cdb095ed54b825fbaa2`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 49.3 MB (49284971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1bcf71e7415358ef282cfd7f21c564f4bb38e7f82265f67841cf7f82742973`  
		Last Modified: Tue, 21 Oct 2025 13:00:15 GMT  
		Size: 145.7 MB (145658364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a296fa67af0bfbef569c06656d5f3644eccbeb6d09287bd99abcea06fdb80d55`  
		Last Modified: Tue, 21 Oct 2025 02:21:52 GMT  
		Size: 85.5 MB (85543183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb33c36ab2c061304653d776cb8df7d6999dfd51a2e5b6cf2e4a8fad95579c17`  
		Last Modified: Tue, 21 Oct 2025 02:21:46 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:52fe46abfaa3bc38b75a72f939d6fbd7d1841c17b3187ea8fe08e7c06ae2a560
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7501268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1531eabb6b66ebf79553982e6dd98a93d8844fbfc09b15772b9761143b0c5593`

```dockerfile
```

-	Layers:
	-	`sha256:0787cde4108112ae81fe04c5858525a36f2ae3f1b2d1edd6b3ff00ed622e10de`  
		Last Modified: Tue, 21 Oct 2025 09:37:39 GMT  
		Size: 7.5 MB (7487040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e66ee8daeef4a314fa8cfa6801bce405c64257b11fcc3f3795574dd689e048a`  
		Last Modified: Tue, 21 Oct 2025 09:37:40 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:44b133d80a5e6b7fc59f2448fb0c643861d6406fab911e8cdf6ba5e95607e498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277473891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eb143c75278eb76f181c0d78d8c671408f9208c795fc9457c2e78b27d69514a`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2033b007fd41cea934872d63ad6c7f44e2c3ad08864553cec3aebe597bb38c65`  
		Last Modified: Wed, 22 Oct 2025 08:07:40 GMT  
		Size: 142.5 MB (142460560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d803fb52b693d7067b3e642251f549a811041e21c8e94a337e25cab0481b381`  
		Last Modified: Tue, 21 Oct 2025 02:27:03 GMT  
		Size: 85.4 MB (85362943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7f8c8c76d57ae55061b3b8abf965ff0baadf44b134ad6b3f5693edda5b09f21`  
		Last Modified: Tue, 21 Oct 2025 02:26:54 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0967e1fcc543e187d60055dc8e124231c6d85e57f5d50d93e40d46b8eb515457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7509034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17ae8e822219bf1729f70aebba17d3004cd3db61a0d57bdb86d1cc5398db4181`

```dockerfile
```

-	Layers:
	-	`sha256:758f9e4a360a93890b679c7192bdea102a66f11fef6f76293ba31fec196f1089`  
		Last Modified: Tue, 21 Oct 2025 09:37:47 GMT  
		Size: 7.5 MB (7494688 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b6dda63790e71a8e87e2e74e1423a0c09afc59827dd004c033453167c97f4c2`  
		Last Modified: Tue, 21 Oct 2025 09:37:48 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:1f52913572128cf785040c98317ccba43d70f5f40f853ce04612963dee260bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.9 MB (276912147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3a7ffa59fb26f058d94118520bd7870817400566b2a2a37f4e7bcdea2797132`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:047d1b265d8a7d20ef8b3ccb9f133c3c5f1e4f9c92089889756590b7f20452b5`  
		Last Modified: Tue, 21 Oct 2025 00:26:24 GMT  
		Size: 53.1 MB (53109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05657968b04d89b7505c556f928a437efac01def053a76ab254d7cdcdf932a85`  
		Last Modified: Wed, 22 Oct 2025 21:58:42 GMT  
		Size: 132.9 MB (132853184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1730185cf0dbdfa5895e271ce04a1f09930e6effbbb2989d3fdd47870d324855`  
		Last Modified: Tue, 21 Oct 2025 15:43:48 GMT  
		Size: 90.9 MB (90948843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1289d75ba5faebde27e1f0969c39970b6afcd916c6e1483d80eb1d2be06fd63`  
		Last Modified: Tue, 21 Oct 2025 15:43:38 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c5e74f38a495a4f34070100ec4bc979a5a5d136c5276bc888d85d89c985ca30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7505119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f8ad5db39d419e100e0c6e7bca15d3420edf469971f63694e907f59c6adc50`

```dockerfile
```

-	Layers:
	-	`sha256:5e7e4bad2d5f6dc3adafc73adcd22d71f911f0bdcc94457de0c613872f38e6e7`  
		Last Modified: Tue, 21 Oct 2025 18:36:26 GMT  
		Size: 7.5 MB (7490844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9164c310848fd6797230747e37d5760ffa5e59128eee5873dbc166278043bb9`  
		Last Modified: Tue, 21 Oct 2025 18:36:27 GMT  
		Size: 14.3 KB (14275 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:c5ac2025ecaf3d9429b9bc3d60d3453bb4b738a07823bad567f8fbd43f5cbac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261481808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b68a89d2af63b6618ea1f7b5793f47deca85fd54e587b0a28ae89dcd2826f975`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:be7c8533c3f8dfcf5ab5c0fd76b47a568dc971c853834a20808defd1e88a5ffe`  
		Last Modified: Tue, 21 Oct 2025 00:27:58 GMT  
		Size: 49.4 MB (49351699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5801e8d44f1ad68bc8796e4f3ad29408782d6c37093ef903520fc5c935c22b85`  
		Last Modified: Tue, 21 Oct 2025 21:47:56 GMT  
		Size: 125.6 MB (125622121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a6f85adec373efaaf3ae479c124e0f06b00ed1c861a46189c065fad7c1d223`  
		Last Modified: Tue, 21 Oct 2025 21:58:38 GMT  
		Size: 86.5 MB (86507343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a1f24a4f2fa3954e4fcb5b6287bb11cd2fc949ce4d8ee053c175ee0756d410`  
		Last Modified: Tue, 21 Oct 2025 21:58:35 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:148fe3efffac759c26411ed67482714e36ff5cc280e27d0495ee0744bb571581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7497194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da362a729d81bb877fca93b750656b6ffd0b30b24477352333b5e0870997363d`

```dockerfile
```

-	Layers:
	-	`sha256:781c3c2a0c8311e5496ec50bb81062eb10ea331349975040cc814d2c03238e1c`  
		Last Modified: Wed, 22 Oct 2025 00:36:27 GMT  
		Size: 7.5 MB (7482966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52feec8061d0d566359d1d65e861e5be7073e73911f544370e7c3bfb8fe0cc5d`  
		Last Modified: Wed, 22 Oct 2025 00:36:27 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json
