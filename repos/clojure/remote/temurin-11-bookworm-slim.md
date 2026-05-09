## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:f4045481aa7d823622febcca6450f51fc5288e49406356d64c471ad290d9ef9d
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

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cecd085619d69c108619a46491a1f2f7b1885c5bf55e6f2d23a8d1c87da1f97d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243822174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8351cdcb6e5f794a01964624229d54633ed6639675166cba38445ab71c9a99ff`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:16:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:16:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:16:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:16:09 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:16:09 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:16:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:16:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:16:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed9285fdb853e019fd5fdf966040efb3ddbb35bb587feeb9b38b60c06879e55`  
		Last Modified: Fri, 08 May 2026 20:16:46 GMT  
		Size: 145.9 MB (145886217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0688193f253d8bc8f555b6cf0d637f49d03ede33f2be81d2518b290a968c6b8e`  
		Last Modified: Fri, 08 May 2026 20:16:44 GMT  
		Size: 69.7 MB (69699033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca05720dd81f34d67e6450fdd39c8315f431065a0c76341fd2c6efb3321f7415`  
		Last Modified: Fri, 08 May 2026 20:16:41 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b69d61da0ba917a3f0e5a1a7a06b9a59bfd86aee20e0f121a7854c95dbf44e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5150730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d0c6ddf38b190b7713f0342371607daab646723aaf15129f091b79fdf22040`

```dockerfile
```

-	Layers:
	-	`sha256:862dda21a219215b23e21e7fac4b6944442bb08732526e3ce20f269d0399f0ac`  
		Last Modified: Fri, 08 May 2026 20:16:41 GMT  
		Size: 5.1 MB (5136310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:969c4dd83de7f7e5bd580479a3ce49ce97ef7c8a77f327dcbaa09cdd5d736823`  
		Last Modified: Fri, 08 May 2026 20:16:41 GMT  
		Size: 14.4 KB (14420 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:411637b8c0320b2688a5fd12ad6c7bfa0812f6124da73631c42a5abc842d68ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.4 MB (240391569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aaf39aca39ed9856bfa7ea95ca4fde0c71d5775b2ce14280dcc953eadfcb5c5`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 20:20:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 20:20:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 20:20:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 20:20:19 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 20:20:19 GMT
WORKDIR /tmp
# Fri, 08 May 2026 20:20:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 20:20:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 20:20:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551f239fea8ded00131393e6ef16e9e5bfb64a6a3c0383c01b5a2d20a1185119`  
		Last Modified: Fri, 08 May 2026 20:20:58 GMT  
		Size: 142.6 MB (142582233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7daed7784b9f64c92bccb0b3bd6a439d6e5196a385f3f9f8ed6e11436db35475`  
		Last Modified: Fri, 08 May 2026 20:20:57 GMT  
		Size: 69.7 MB (69692525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fefff4fe25cc85923b567eef9552a6190ba2bfe61a84905f870e797841e260`  
		Last Modified: Fri, 08 May 2026 20:20:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:74e2f277c4eb69bddbb64944cbc88d55985900122875ea0b5a0f8da2afbe3e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5157228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:387954402da28e3d7e35c448e6c69e3e9ddc1cf9a54cc00e29ef7bac8d589824`

```dockerfile
```

-	Layers:
	-	`sha256:1534478f4bed9db5fbecf9e733bdde8fa066a9e632a226b4f7b056eb18f35f3e`  
		Last Modified: Fri, 08 May 2026 20:20:54 GMT  
		Size: 5.1 MB (5142689 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b51f57f6bf626e4d17d4cc294a0f107a2a1b2233c1e9a698be394ae4756365d`  
		Last Modified: Fri, 08 May 2026 20:20:54 GMT  
		Size: 14.5 KB (14539 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c9420c0a8a5d8f0f6374b93f18da2a16168dff3239ecc17b4e5b1ffb3d5b6d16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.7 MB (240718747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d4a15c6aef00a89ddd7d207ca55fbfcb4cf470c003b04b8c291a02a5eca63d`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:25:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:25:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:25:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:25:33 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 09 May 2026 02:25:33 GMT
WORKDIR /tmp
# Sat, 09 May 2026 02:28:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 09 May 2026 02:28:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 09 May 2026 02:28:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a6cd9ce9367000978e62d727341fdbe8bd162e7346e254771317696df2b498`  
		Last Modified: Sat, 09 May 2026 02:26:34 GMT  
		Size: 133.1 MB (133110215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa10e0fa10c5474f57cf19ca069e11f7fb8703595391ebe214d16226afd75bf`  
		Last Modified: Sat, 09 May 2026 02:29:08 GMT  
		Size: 75.5 MB (75529434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af165a08b928834eefa867a20bc3c72ece7a9b18db758cc0300439c4080938a8`  
		Last Modified: Sat, 09 May 2026 02:29:06 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:00d942bcea7fedfd3ee41d11821b8304e397510cf65cb259759a475fb21127c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5155321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77a3987723b7f9a408266acee835a2b01daec2428e83b8876200e57af2e3d7c`

```dockerfile
```

-	Layers:
	-	`sha256:410f307e60b3871325b8bc73efa522120838b47aef16af7032c88fdf87baefab`  
		Last Modified: Sat, 09 May 2026 02:29:06 GMT  
		Size: 5.1 MB (5140853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:804370377fd69e3150da5ce063103166822c213d850ee959ab68cb68f3408c22`  
		Last Modified: Sat, 09 May 2026 02:29:06 GMT  
		Size: 14.5 KB (14468 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:4104e27a3df9d747faa2b3e4bcc7cb02e9dc933f1f7cebe955d2b3e012f6c335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.1 MB (222057000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afaf11d6a871eaa5bd13f816f31edca920ea8cc78829f5ab96dd4ade16c5d119`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:12:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 22:12:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 22:12:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 22:12:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 22:12:56 GMT
WORKDIR /tmp
# Fri, 08 May 2026 22:14:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 22:14:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 22:14:14 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ea993f684cb01e3eea5d725a6fc9f80d3d869ccf66211510f5ac3a0bcde03a`  
		Last Modified: Fri, 08 May 2026 22:13:35 GMT  
		Size: 126.7 MB (126651719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1b44f01ec1b05041844367f11f3a66a118b3e67ac818eb585da2791700210d`  
		Last Modified: Fri, 08 May 2026 22:14:38 GMT  
		Size: 68.5 MB (68513035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b72021a3fc38e9b98f44ebfc3e7eeffe0bd2786877d36d69b12d2a63b02d35d`  
		Last Modified: Fri, 08 May 2026 22:14:37 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aaa8a939bac0d48ef1abfd98806921a47f589ee0e9c201787bb3dbb31419b3f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5142056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0167fac546047206f730c776a06fb8c248b9b37380bd8d7948c536b9909bbfce`

```dockerfile
```

-	Layers:
	-	`sha256:935323d673d749e6a63518382af2debe6d27d80342be5a1a95aa355db9408cd5`  
		Last Modified: Fri, 08 May 2026 22:14:37 GMT  
		Size: 5.1 MB (5127635 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6029465f4e59d3d021984aced422be17c85c8c0b87b1108bf8803093905fbee`  
		Last Modified: Fri, 08 May 2026 22:14:37 GMT  
		Size: 14.4 KB (14421 bytes)  
		MIME: application/vnd.in-toto+json
