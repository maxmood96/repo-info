## `clojure:temurin-11-trixie`

```console
$ docker pull clojure@sha256:d3f3c07e08e70fb3eee7c1f3c6024f376a4b59c72c119fb716425cd0f5dfbe3e
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
		Last Modified: Tue, 21 Oct 2025 02:26:49 GMT  
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
$ docker pull clojure@sha256:672c0281fa68c88ce482b4c527bc8e4d0a40094fab48a0b247a39fad4fd383ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280114456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:718657a85c02262944d02d386aeac8eeebca70c93b70f87e62da0301a1deee86`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
	-	`sha256:71fbf24a239310917388930bb043e64907cb532b9ac8f265e44e032dc3bf4409`  
		Last Modified: Mon, 29 Sep 2025 23:41:05 GMT  
		Size: 53.1 MB (53109217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a82b02d8d33edc9a575f1806b6648d43f0a3b10a8a639821640f289e379590`  
		Last Modified: Sat, 18 Oct 2025 08:29:19 GMT  
		Size: 132.9 MB (132853221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0775bd8202147f0491340d2c225b4dce77a8e14acc2655dd2fc172fdff8a1b8`  
		Last Modified: Fri, 10 Oct 2025 05:12:17 GMT  
		Size: 94.2 MB (94151372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d21081380a341575e0c4a732931b03e3c21153d126e32320bb75cc10a7386d`  
		Last Modified: Fri, 10 Oct 2025 05:12:04 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6d59cdf968b6901117f6077634040c068c5f063f4024826921374d89992c6ea7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7505119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0cadd4dd46320c26a639e790d3842d825b7a6e53ecf6a9dcd9915e7a2d12c9`

```dockerfile
```

-	Layers:
	-	`sha256:0e2f3a0b90662202897f08cdda629d7c26362aca9ec6417e435d1cbc207bbff5`  
		Last Modified: Fri, 10 Oct 2025 06:39:05 GMT  
		Size: 7.5 MB (7490844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf423cdf476728c3605416d44f0dd001dded9c2b81692cd94057690a701eb42f`  
		Last Modified: Fri, 10 Oct 2025 06:39:05 GMT  
		Size: 14.3 KB (14275 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:55b6bcaee8da1c695ac5b19d87f3325e738928bf0eabb32d71d68a9ebd154987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.1 MB (264099411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d158caf78426bcf85df577a641deebeda971fe5861f1e3aa18ab2cd6a7a1f31`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
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
	-	`sha256:024d6c344f0b9dbb2baf07e95dfd2abbfadc5c8262ca381f39f6489670cbaff5`  
		Last Modified: Mon, 29 Sep 2025 23:41:06 GMT  
		Size: 49.4 MB (49351442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84f66a0fc9c354ca1f63065e761ed625868322e7e3a30084169fe6d34e33876`  
		Last Modified: Thu, 09 Oct 2025 22:54:23 GMT  
		Size: 125.6 MB (125622160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22cf04f3c08df2823ca8a1f1641181924d46b50609de21210d4ec089ebfaff3`  
		Last Modified: Thu, 09 Oct 2025 23:06:12 GMT  
		Size: 89.1 MB (89125164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e046f6c8357e5e2bbb4effa2c268362293a5af2fb84636cacdab97b7e8f82d8f`  
		Last Modified: Thu, 09 Oct 2025 23:06:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0fcfd642ec1fe3fb3b9d45a3325811e31d0ed7e9d78d9dc9b4c241c5330a3fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7497194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34822fba9b35aef16f88af40d3ce0a8bc602abdf47b7b28693f1a1e152e4b026`

```dockerfile
```

-	Layers:
	-	`sha256:c229a421def7425a7e30877702ace97054545ad89af73328d44c844eba358223`  
		Last Modified: Fri, 10 Oct 2025 00:36:55 GMT  
		Size: 7.5 MB (7482966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e18f62575903df59fe3055f658f6e630fc7561dd81cbb3ab5b0f1db4d0fbdbda`  
		Last Modified: Fri, 10 Oct 2025 00:36:56 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json
