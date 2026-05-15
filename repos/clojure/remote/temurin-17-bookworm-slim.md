## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:d2500d96cd675e31b2ceeb7e965f81435a06784e0d1c5629b4bdbcb568f29d4b
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

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1cda869c8857e516b905f896542ce7bce5ce8988836af4b600ff2c02f42bad9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243873313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bef87e67e12e0e194fb91ff7cfe565d98cd3fa8cd94bd1ccad3c5a0abfea3b3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:35:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:35:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:35:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:35:05 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:35:05 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:35:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:35:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:35:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:35:21 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:35:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70e4b07698f1229bf43c5188d8329829ee0524d7f1b1578a2c1a23bd97462f0`  
		Last Modified: Thu, 14 May 2026 23:35:41 GMT  
		Size: 145.9 MB (145905480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdbde9db330f57a088eb81f124b580330858295837623530ea977ca35a30e90`  
		Last Modified: Thu, 14 May 2026 23:35:42 GMT  
		Size: 69.7 MB (69730507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4cd26464b0908de5fc6f9f4e381108de4ce791ad716465c267f0daa14f10e84`  
		Last Modified: Thu, 14 May 2026 23:35:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69367c104e7e5436bd389048ef52adb440ad1af197d32bb89b86367d7693f2fe`  
		Last Modified: Thu, 14 May 2026 23:35:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7a631275013630bdd81765598454469df882edc03b79d92232892090e72191a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22dcaab9ac96b29d811875a93e407e9fdd456a719d30416eae9a032de5095d4a`

```dockerfile
```

-	Layers:
	-	`sha256:b317a50762e42b768628474df82b4ae9d27861affb00d9ea321afede055f846f`  
		Last Modified: Thu, 14 May 2026 23:35:39 GMT  
		Size: 5.1 MB (5116792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d60eada1f695ab12263c8140d163631894d5619b69b2edc0f8f96693347046b1`  
		Last Modified: Thu, 14 May 2026 23:35:39 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:54e73b998511547e11a3c515d0b9f75a08d6a3dd5580acddd2520ad05d5873fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242563806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c671e5e90303ce93464f3d5f2cb0f21f7d933f17f67445b5bbe716e6bb4b21b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:34:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:34:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:34:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:34:59 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:34:59 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:35:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:35:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:35:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:35:13 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:35:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7268e77fe00c1a52120139d4c4b1f7feed4cb19a0d0d4ede0e9bc36db98df2`  
		Last Modified: Thu, 14 May 2026 23:35:36 GMT  
		Size: 144.7 MB (144724335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e7738c2e5dedd7760efbfc91ff8b9740c489d38a51129a6dcf55ae967bfc49`  
		Last Modified: Thu, 14 May 2026 23:35:35 GMT  
		Size: 69.7 MB (69722263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f61dbdebfd76dcb2b979e37c5a913b1d965b056c8c699389bab5ef33a3193c`  
		Last Modified: Thu, 14 May 2026 23:35:32 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ba5f68bd98fc8c0caa6f5eed60e9f694993d30fb4148d569f33f07d23d86c1`  
		Last Modified: Thu, 14 May 2026 23:35:32 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f66d38eaa2e88a5d55b9decf4102af9a9ae80dee88ad5028624b2117cd93df66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:819da64cd24fb8aa1e8a2bfc5aea0678216b450708635dd6ee2c05a2843840fc`

```dockerfile
```

-	Layers:
	-	`sha256:adff5588df7c95cb1fb34aec45057639e9f23ff49519cb782384b3eed7b9c6a7`  
		Last Modified: Thu, 14 May 2026 23:35:32 GMT  
		Size: 5.1 MB (5122553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d00b5e4462c154c48925824fbbe85b881c5d01ca010608fb7cf1cfd81a5c66d`  
		Last Modified: Thu, 14 May 2026 23:35:31 GMT  
		Size: 16.1 KB (16108 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:3c0c19442641b096acc469ecd5b02bac9f85973ab4371368b247d230c03a38e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.4 MB (253411634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb54aa307bec0850276f24cd6ffcf7159d84f8067f22c4586da5541f67f21a31`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:30:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:30:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:30:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:30:41 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Sat, 09 May 2026 02:30:42 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:43:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:43:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:43:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:43:33 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:43:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebb50b599e2de909acaf0c0d8a3d5a70b8d0e3b34206b32960ca5e3061a8a17`  
		Last Modified: Sat, 09 May 2026 02:31:50 GMT  
		Size: 145.8 MB (145766111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c247b9a10a438044ef46232ea7b797b13957915ed48e1d0dfdbb57bec0e75ed`  
		Last Modified: Thu, 14 May 2026 23:44:07 GMT  
		Size: 75.6 MB (75566021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6603c9af34d5fd9deed54ff7c07b4991a6712c4db3d65b33068ce0e102de9bb6`  
		Last Modified: Thu, 14 May 2026 23:44:05 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e4dd14784c5a3cf94e8a386fd4334d14fb4803aaf490ba0a5cda4a847dbc98`  
		Last Modified: Thu, 14 May 2026 23:44:05 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e3d9a43fe8f74edc6759a0f32050362ba717c50eb2aa318387492bc75a16b300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6241bf19996320e089cab9905ffbd4cfb4f53432cf3aacc991a662bf50c9bb0d`

```dockerfile
```

-	Layers:
	-	`sha256:1a1aabf956a4d2368e290f3b5afb7b15e8ea578e8a64d042c2d847b7c8b4be25`  
		Last Modified: Thu, 14 May 2026 23:44:05 GMT  
		Size: 5.1 MB (5121950 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4529d3fea24f270da3481855ae99547f23e378027ace03353b9164c8f872ef2`  
		Last Modified: Thu, 14 May 2026 23:44:05 GMT  
		Size: 15.1 KB (15083 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:e7e99f446907aa65329d9ebcbb04d894dc7f577d79c44fb5525d9fbbd5320dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231347317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1844230957a592100f1e4b7761090f56384db3b27faab39f7f72d6eee315e99`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:34:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:34:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:34:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:34:38 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:34:38 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:34:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:34:51 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:34:51 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:34:51 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:34:51 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5694fd2fb22af8aa0f8c7978432e9a19d6412a485716d6faec12db03eb508801`  
		Last Modified: Thu, 14 May 2026 23:35:20 GMT  
		Size: 135.9 MB (135910447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635b054dd3e40cc86c8f101024bbb532eb6c8740fea313d0197558bfa37990fb`  
		Last Modified: Thu, 14 May 2026 23:35:19 GMT  
		Size: 68.5 MB (68544225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a87f619bf2014b97f7f53f43fc198ea36f6948bfef638a8e6c1e704ad87cf0b`  
		Last Modified: Thu, 14 May 2026 23:35:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f420e655b8e94e88a149f20851ba42dfbca8be1d4432d19071dcc0252585547`  
		Last Modified: Thu, 14 May 2026 23:35:17 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:56a5242cdf9fc38b467629ed84280a2184e49d6b40f7c82e193582d49562c383
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5124103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c7ef452d538ee8bbb74a02a00609a9a5e9b565392498faabc386900cda643b`

```dockerfile
```

-	Layers:
	-	`sha256:b5eb5c28d92cde9f1c9ba2ca18472500f0ed91a8d8a640e33bf2ab96a270d85b`  
		Last Modified: Thu, 14 May 2026 23:35:17 GMT  
		Size: 5.1 MB (5108113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a43315113952c427bf85d71679b7d0fe77e33b0dbfffc80aa2e0fc9fd523f6ed`  
		Last Modified: Thu, 14 May 2026 23:35:17 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json
