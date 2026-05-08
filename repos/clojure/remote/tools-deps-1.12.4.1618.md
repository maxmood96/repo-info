## `clojure:tools-deps-1.12.4.1618`

```console
$ docker pull clojure@sha256:2311253ef04bcc8044f68f084e2a358c451e9616f5efd3b72afb40dd6be349b0
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

### `clojure:tools-deps-1.12.4.1618` - linux; amd64

```console
$ docker pull clojure@sha256:b88407ef46dad69970f93b673c321517665cc3bdcb80c11f9bb1f1ec745898b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.2 MB (222230518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c67a50797eda4b241836596619d3cff5b4a2e7dd50e7ff89415ba0f03e045d54`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Thu, 30 Apr 2026 23:53:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:53:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:53:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:53:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 30 Apr 2026 23:53:16 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:53:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 30 Apr 2026 23:53:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 30 Apr 2026 23:53:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:53:32 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:53:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb5421a313ce2cde5353fb1b8a66e49a22fa2c651de0bf07414e0650abb5719`  
		Last Modified: Thu, 30 Apr 2026 23:53:55 GMT  
		Size: 92.6 MB (92574598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f81d8653ec7316956e5ad88aefcd5c2720d3d01aec181b11c7cf1ebf8bda6d`  
		Last Modified: Thu, 30 Apr 2026 23:53:54 GMT  
		Size: 81.2 MB (81166253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942048aa51229097665a2608e30b84af147d5f0cbc489485ce1d9be6ff7d8938`  
		Last Modified: Thu, 30 Apr 2026 23:53:51 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e4c90c63e1eaef239a5765f29195b046a1f67d4dc76b760905ea42179bd8c5`  
		Last Modified: Thu, 30 Apr 2026 23:53:51 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:1d329b1e533c7a8677e0101db8016560f62bc49754f440cbe5bc2d0295a48082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7366094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c56674445f3ec7717b499b687f7bfab1d8e4e70392971dccd1f2625d7983a49`

```dockerfile
```

-	Layers:
	-	`sha256:f44d37ec0c2f0281b6d91daf287a672fe008d4f399f20ea094a908ec0f6f5e34`  
		Last Modified: Thu, 30 Apr 2026 23:53:51 GMT  
		Size: 7.3 MB (7348323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44c9b9f9e8d92684f77b93f101213535300df901432735ec4d909780ad3f3457`  
		Last Modified: Thu, 30 Apr 2026 23:53:51 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:05ba31ac8806fd03c0480952cf383d0b2e4f86926a4a3beaedbdda42235230e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221090994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2a8a40e129eed38b4f3ac23d1f19fa8a7de64f24b14c70ea5cac33315a340d3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:27:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:27:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:27:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:27:35 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:27:35 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:27:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:27:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:27:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:27:50 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:27:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240c60651ab3b90f7967d6b86da04653ae3eac26d37b03df59a2c18a6a668424`  
		Last Modified: Fri, 08 May 2026 00:28:13 GMT  
		Size: 91.5 MB (91542275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86996a8f9adc73e9c3afb68d7c4cdf55d8f3cde2389893a1f198ba7d38895d56`  
		Last Modified: Fri, 08 May 2026 00:28:12 GMT  
		Size: 81.2 MB (81174607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8264abf60fe26b0013a15dc27ad9abe317bbb8c1c2902c4f9f9398d3c71aed4c`  
		Last Modified: Fri, 08 May 2026 00:28:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901c0b754bd06838472f75f36ce5d957ae52f4dfc5f064e6d80c878a5727bc96`  
		Last Modified: Fri, 08 May 2026 00:28:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:e2aef8bcd2a2cf2129e4ed8ee6c4bbe02d29b7825a14107c83480306df005f96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7372270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986b13c69c77e6d74ef6ae61ea22d0565f83da977c751d78a0ebef8b0ec845f7`

```dockerfile
```

-	Layers:
	-	`sha256:f7e33f87c665059d437c42bbca7570899b4c47883aacf0fa55e178d435fb14c7`  
		Last Modified: Fri, 08 May 2026 00:28:09 GMT  
		Size: 7.4 MB (7354155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71b7ffa91462644854b1ff69f7fc5d66dd6e57385ae84c216ba82a5e2cce523e`  
		Last Modified: Fri, 08 May 2026 00:28:09 GMT  
		Size: 18.1 KB (18115 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618` - linux; ppc64le

```console
$ docker pull clojure@sha256:5ca6e21ec8eaf5386f4055b9f26ff9ecec5883b62aba9a20c8b0655a16c7758d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231255934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8051b3e66edc517d1ec2345a19d190701d9750d605551a6df41387d501ea540f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 01:34:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 01:34:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 01:34:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 01:34:38 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 01:34:38 GMT
WORKDIR /tmp
# Fri, 08 May 2026 01:46:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 01:46:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 01:46:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 01:46:05 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 01:46:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d733e476aa8595c677a7a8e78f0fbc11c82e45660c7657482695df3b0260f12`  
		Last Modified: Fri, 08 May 2026 01:36:27 GMT  
		Size: 91.9 MB (91913990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3734258ae6f0879085c33ac8bd8c005607a12fc9792e1606358bab34ac31e5e`  
		Last Modified: Fri, 08 May 2026 01:46:40 GMT  
		Size: 87.0 MB (87004167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c5c45b86b42c3f76314bbb018a424f1fbef2434b8448febfdf6bcb39acf3b41`  
		Last Modified: Fri, 08 May 2026 01:46:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfe34faba218d866b7acf8c6f233eaab0559ed9bd9848c600dee559c0620294`  
		Last Modified: Fri, 08 May 2026 01:46:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:d1c5636d5a22349b89091fc05729b3d63b4e14f0ad2d930151b866e33409ef7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7354896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac06e2488b4cf23097ca3e75ced647dd1dc288ee15341c1b831f10659ea25ba4`

```dockerfile
```

-	Layers:
	-	`sha256:58cf8027d74f46e0b63915f5a152718e38bcd5509c4a5b1020fad193b34437fd`  
		Last Modified: Fri, 08 May 2026 01:46:38 GMT  
		Size: 7.3 MB (7336887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8acf40dddc186dbf352975542f25e9ce5b8fa7cfff8da169b3410ff0767a1780`  
		Last Modified: Fri, 08 May 2026 01:46:37 GMT  
		Size: 18.0 KB (18009 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1618` - linux; s390x

```console
$ docker pull clojure@sha256:f1852669bef247377c0f7e9dbb95c438fa66638f4434c034b825d7ace63b7b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.5 MB (215549131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb89d426bb7e63e1fb3b6e618f7042a5044ed1e0a12f21b6b636277d5fde2fe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Thu, 30 Apr 2026 23:49:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:49:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:49:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:49:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 30 Apr 2026 23:49:40 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:51:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 30 Apr 2026 23:51:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 30 Apr 2026 23:51:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:51:15 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:51:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439ca7a271e362a7945b93efef6e6eb132b28afbec5dd9a21f35ce6c32acb6e9`  
		Last Modified: Thu, 30 Apr 2026 23:50:59 GMT  
		Size: 88.4 MB (88420341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ac5e1057de4c48e3cea6fda372d2985436cb702d4a2f54363fe6287d134c10`  
		Last Modified: Thu, 30 Apr 2026 23:51:43 GMT  
		Size: 80.0 MB (79979779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9a84e1e3d13a19798e48c174ee59526237b025b49223ee4ebc0a2eca02fc4f`  
		Last Modified: Thu, 30 Apr 2026 23:51:41 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1b62ff34976f2f97a894608dac4e2f5dfcbc581084517b735e6d2bdd0665d8`  
		Last Modified: Thu, 30 Apr 2026 23:51:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1618` - unknown; unknown

```console
$ docker pull clojure@sha256:b14437fe5f5ee49194f2e5c2d975d09f3925d5e7f9be3d24e83b27901a170e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7341975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3724bc8eda7b070d8975f0141e745cab9a6e7d848fa866fbd587890e71b197`

```dockerfile
```

-	Layers:
	-	`sha256:292946717a082e8e3f2dc64566e2db93875f927ab53c836ee9842de295040164`  
		Last Modified: Thu, 30 Apr 2026 23:51:41 GMT  
		Size: 7.3 MB (7324204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df185fd24e2470878ff544da9c8acbb29bee150fea955cd5eea92fcc3ddd56f3`  
		Last Modified: Thu, 30 Apr 2026 23:51:41 GMT  
		Size: 17.8 KB (17771 bytes)  
		MIME: application/vnd.in-toto+json
