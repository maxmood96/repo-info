## `clojure:temurin-21-tools-deps-1.12.4.1618-trixie`

```console
$ docker pull clojure@sha256:92ecdcc40492cf15b34140e73592fdb9c79807ebe9b9cff30dcf74e3952c64b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:98a0bac602f24c1c9351c49e1326373a62ebdaf8634522d89e2132c459b801e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292723133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf9bba4a868f6a031671d7aca23565f20e9b029d0216c76a553b06a33697078`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:00:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:00:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:00:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:00:07 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:00:07 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:00:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:00:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:00:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:00:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:00:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7a100f13d90800f692a70eef1f73ec694912a446cb14147df3871fb76c0572`  
		Last Modified: Tue, 17 Mar 2026 03:00:51 GMT  
		Size: 157.9 MB (157857091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ae0d663d3fd7950dcdeef659bf701f3fb3e93b3502b6517247e825bae4c126`  
		Last Modified: Tue, 17 Mar 2026 03:00:50 GMT  
		Size: 85.6 MB (85567473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a63501803f3bb719627416f7edf2f9ce2f54b46755fc919d131576aef893da`  
		Last Modified: Tue, 17 Mar 2026 03:00:46 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60cc3b2d8fbdb03f8690aebdeb9d54565897553413670333640ed59978f1e61`  
		Last Modified: Tue, 17 Mar 2026 03:00:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:57680de3e9ade646475f29ef0b76fe9f630bf0b2dd77b315b64c5eb4680cfd34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7488271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:221b956bb01a88d11a334f70b15f8b0143ec624024331192581a6d3a26e6ff05`

```dockerfile
```

-	Layers:
	-	`sha256:dc3c9af0299be0acc238c8c8e859119287b975728c892ada4a7481b7aca2b2ae`  
		Last Modified: Tue, 17 Mar 2026 03:00:47 GMT  
		Size: 7.5 MB (7472519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:940d2a0d7f64e2df25e21f23394fc913baf61af617fd5eb8d195f5d9639a6508`  
		Last Modified: Tue, 17 Mar 2026 03:00:51 GMT  
		Size: 15.8 KB (15752 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0c07d0c3209a35623cdd88d5998e87dd7181fcc3e3a415487ff2368965d8e646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.2 MB (291182073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d5bc3b5d1d14b694ad49e44f86c47bc80e64c1a0dd309f54826fc91958988f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:05:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:05:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:05:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:05:02 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:05:02 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:05:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:05:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:05:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 03:05:22 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 03:05:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1a1b8892bb821d9f48fb25fb3f386c367660eac5f16e51aef090a1b1419a4f`  
		Last Modified: Tue, 17 Mar 2026 03:05:48 GMT  
		Size: 156.1 MB (156133026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80163bc518f2c9d86de3939b261a3cca96cc72b3777c9f2e1c3a9d37d3a0abaf`  
		Last Modified: Tue, 17 Mar 2026 03:05:46 GMT  
		Size: 85.4 MB (85383053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeb5b3a791c73221f5e230cf2237cd8554ea0f11f39c77787e55b3c93d227a05`  
		Last Modified: Tue, 17 Mar 2026 03:05:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edb0e089fb4c2472cee1539cd07b59b7e2430222befc7f73725a9a2169f5af5`  
		Last Modified: Tue, 17 Mar 2026 03:05:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e020cd932ebfb5e355c57046d1dc0dff1c3d158a7f0a7033c51df3dd380b7f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7495421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5a9e86de3919852ab98a247767ac29d73e8e7944df02dfc7c9bf4facf22ac1`

```dockerfile
```

-	Layers:
	-	`sha256:65f4ec251eda420e130559254ced60ebeb088c04041c41f8f3af676dc0904c78`  
		Last Modified: Tue, 17 Mar 2026 03:05:43 GMT  
		Size: 7.5 MB (7479549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:406d779cf92959758ac6330c6b6da221b7ee3bd6303d64e5513ca6c69b6920bd`  
		Last Modified: Tue, 17 Mar 2026 03:05:43 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:00dbea6cae588d439b384813701fb794c55099ba48cbe2017b638cd86648197c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302067502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1688211606ccf65cdc151aeb86a78c25b583747bd3304fa90e8b56441e692243`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 21:03:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 21:03:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 21:03:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 21:03:29 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 21:03:37 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 21:04:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 21:04:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 21:04:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 21:04:58 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 21:04:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecbee4d241c3e51c5833536e2a14e47748e3bf7f3563306f4afbb22a0345981`  
		Last Modified: Mon, 09 Mar 2026 21:05:58 GMT  
		Size: 158.0 MB (157977504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09986865d66dfeba3d3d1695420da6e5e9872d43ce93ee67de46b6ebe9eaeefd`  
		Last Modified: Mon, 09 Mar 2026 21:05:56 GMT  
		Size: 91.0 MB (90976694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993ece8f9a9cd48b3c9721bd6417438b9bd874f99e54d76fd14f7c1fac0660c2`  
		Last Modified: Mon, 09 Mar 2026 21:05:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805996622cedd24a9cb8c2df1a9d188766eebdae407a399ccad7edbab330abd1`  
		Last Modified: Mon, 09 Mar 2026 21:05:53 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:26799df9d51baa5d5894731a5bd67cf67ae471f76d225f079bc040f668a3408b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a60d2ba0c4f2e7a56dbb7cc141401082ea94ecb0e2a3837550e87918aac547`

```dockerfile
```

-	Layers:
	-	`sha256:04dca80598934e9eb060f6dbc5571a15ec977a22de17bf3c1b008bda3fd58118`  
		Last Modified: Mon, 09 Mar 2026 21:05:53 GMT  
		Size: 7.5 MB (7476866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0649854a198b65f383f41da4137c4b2a8648b3f5934ae1bcc3943a814a764eb5`  
		Last Modified: Mon, 09 Mar 2026 21:05:52 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:b2bee7d1b945bd20090753b55d3200431df96f9c614b6be607205e00c4878c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289447514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bfac613d180309f0bd327508635ff00cf128064f8b30d3ab36b36aa88ee42dc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 11:14:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 11:14:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 11:14:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 11:14:59 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 04 Mar 2026 11:14:59 GMT
WORKDIR /tmp
# Tue, 10 Mar 2026 01:38:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 10 Mar 2026 01:38:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 10 Mar 2026 01:38:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 10 Mar 2026 01:38:21 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 10 Mar 2026 01:38:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3be247472b67578a1d05739722d8adeca41098796e5d6210800176db58046fa7`  
		Last Modified: Tue, 24 Feb 2026 18:57:42 GMT  
		Size: 47.8 MB (47776936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb9c79161005e6b84d0763b0f118c07cedf15f1b6ee06d958a2a83ad03907d3`  
		Last Modified: Wed, 04 Mar 2026 11:23:14 GMT  
		Size: 157.2 MB (157216889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d5d02f7b83844a0868dd8f028cb57a1e57e909bef42be92d11b6b50e8b301d`  
		Last Modified: Tue, 10 Mar 2026 01:43:41 GMT  
		Size: 84.5 MB (84452643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f29f76ac2f6c85f320d15da81852d9b4131e3fb9a62e14d0c95e9f4d9e16a1`  
		Last Modified: Tue, 10 Mar 2026 01:43:27 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d656f73699437c686c7a8edda71370a40c3be091dc8b87ec77acd4c2319ffc`  
		Last Modified: Tue, 10 Mar 2026 01:43:27 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6fb342b904061038b1b61d44537c3e2e39c0338c8a08809c5eff2a3b48c26746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7476160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b03329ddf893905ed1fef04f18932e04dd75b3098945e999cd352187ff79adfe`

```dockerfile
```

-	Layers:
	-	`sha256:fc6d338096b4c6dbf524de47838de6061d4aa15e54e11e3b58fc32919a5e20c6`  
		Last Modified: Tue, 10 Mar 2026 01:43:30 GMT  
		Size: 7.5 MB (7460360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:936695ff712e2e37b93456b0d5ed96435c0c60768ba8ae6c350f8c343eb4e556`  
		Last Modified: Tue, 10 Mar 2026 01:43:27 GMT  
		Size: 15.8 KB (15800 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:ae26bff066eebe4f55ac67d2bbc809b7928fb5f318407901942c833081650e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (283015628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64443c07f5698a7327eecf9001fae2336a966278f1766ecff73927a633191cea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 11:42:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:42:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:42:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:42:33 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 11:42:33 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 11:43:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 11:43:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 11:43:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Mar 2026 11:43:22 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Mar 2026 11:43:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7bc76783a6155f9347e92234e4b5c38bd02638c6de782f4623d0736c769250f0`  
		Last Modified: Mon, 16 Mar 2026 21:52:57 GMT  
		Size: 49.4 MB (49364775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f17a655283acfd5026e7bf35bfd3c21747c0f9fb4e21fa04b1ee69e7f604fe`  
		Last Modified: Tue, 17 Mar 2026 11:44:04 GMT  
		Size: 147.1 MB (147105214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65387c4743caf12a89286e17c561a423bcaf63c97d5d1430d95039eb2163ccd3`  
		Last Modified: Tue, 17 Mar 2026 11:44:06 GMT  
		Size: 86.5 MB (86544597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b6f27b6da33e4a9b477bc53a4c1042f9da11892859f4cd9c04212a4cab40cc`  
		Last Modified: Tue, 17 Mar 2026 11:44:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46029984f0dc7ee3bff89aebfadbcda447a9b27ef3215abbd650e94c612fb53`  
		Last Modified: Tue, 17 Mar 2026 11:44:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:524779d51e72f3373cb4ce625b19bfb21bf415fa485fecfa09a38388a7c4a85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7484195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59f1febf825db90f49774ee1733f396284accca9a96d78d98b32b123003f492`

```dockerfile
```

-	Layers:
	-	`sha256:1c16107e53c34cce562b4652697650af7b5a77da4855041ea6504290108f8973`  
		Last Modified: Tue, 17 Mar 2026 11:44:04 GMT  
		Size: 7.5 MB (7468441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a62bb978f01adff0139eb4f7936864cf7439784bb3b62e565946ba5501eca5c`  
		Last Modified: Tue, 17 Mar 2026 11:44:04 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
