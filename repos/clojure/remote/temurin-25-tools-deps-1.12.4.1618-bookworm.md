## `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm`

```console
$ docker pull clojure@sha256:2fda4519f784b4ae71267ea4c41f5fa85e05c076cb771156edbe1e3d64e8884e
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

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm` - linux; amd64

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

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

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

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:64a7a53bf2cbcddd1221628ecce2ea223eca2397717b218cd70621a0decf93e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221090435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e4523ba02c443e729dc369cad8e068303866bffa255266c9db4cad9afefa8b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Thu, 30 Apr 2026 23:53:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 30 Apr 2026 23:53:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 30 Apr 2026 23:53:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 30 Apr 2026 23:53:12 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 30 Apr 2026 23:53:12 GMT
WORKDIR /tmp
# Thu, 30 Apr 2026 23:53:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 30 Apr 2026 23:53:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 30 Apr 2026 23:53:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 30 Apr 2026 23:53:28 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 30 Apr 2026 23:53:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc40333aed8730c21bed3fc86b30ae25003d557055752daff740ef9ec6d401e6`  
		Last Modified: Thu, 30 Apr 2026 23:53:51 GMT  
		Size: 91.5 MB (91542288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9fa9ea86f57b71ac25e7d5f9f20c08ba5900488a3ebf750db86d618bafd5862`  
		Last Modified: Thu, 30 Apr 2026 23:53:50 GMT  
		Size: 81.2 MB (81174037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91feae5a0ddb7b21938a32ffdafb3dec8637c4479f8e93095c736c0620952729`  
		Last Modified: Thu, 30 Apr 2026 23:53:47 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ee7efd702392a5e7f2a136f4bf35512156e900b9df3cab1225f3b6643b32f8`  
		Last Modified: Thu, 30 Apr 2026 23:53:47 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e08256062a2c1f28ac30001b41c617552b212851809fef1339fab2c7e0a4e20d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7372116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0daff75608191ae0eafd2b1ac783feab40fc9005fff203e9f2af512ee1d6644a`

```dockerfile
```

-	Layers:
	-	`sha256:e0d0d27a6660ef9f1605e9b20b585ef5409ea719a23943120fc287c8c14a5ddc`  
		Last Modified: Thu, 30 Apr 2026 23:53:47 GMT  
		Size: 7.4 MB (7354155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ef6a83a98c64d673e5a972cf4a358f69a259a58500d095c00ec7ae0aae3c857`  
		Last Modified: Thu, 30 Apr 2026 23:53:47 GMT  
		Size: 18.0 KB (17961 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:9da7e2e4e75104e1922975799813adec2db1e3dfaf8afbf1785d1e2c641ba8c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.3 MB (231256218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5623dbf1b6ee5458c8def7b2561b5a65d10db0da5409f87433cadc02c8a2e089`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 01 May 2026 00:07:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 May 2026 00:07:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 01 May 2026 00:07:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:07:11 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 01 May 2026 00:07:11 GMT
WORKDIR /tmp
# Fri, 01 May 2026 00:13:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 01 May 2026 00:13:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 01 May 2026 00:13:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 01 May 2026 00:13:08 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 01 May 2026 00:13:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01487bcba0d0c1649162f2116f011092d3effd12c3f381faa370fdd01952d8b6`  
		Last Modified: Fri, 01 May 2026 00:08:34 GMT  
		Size: 91.9 MB (91914030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9f555cc982c34f18950a4bac6a84cf3511fae470d1424a0d036df758ce3b35`  
		Last Modified: Fri, 01 May 2026 00:14:08 GMT  
		Size: 87.0 MB (87004410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d662ed7b26206f8834776593a459850873c333b8723896a6e5288450cc30d95c`  
		Last Modified: Fri, 01 May 2026 00:14:05 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e428b69270cc6d04295fcba960a4d5b22e7e325bb202867065d4d58f5e3cc828`  
		Last Modified: Fri, 01 May 2026 00:14:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:59423c245772dcdb60bb1300f731edd4f61df9533e90e9e15769ed698e213ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7354742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0be28ecc36e408ff7f8324b74a224a6306253caf372d982a3d31f19dade6193a`

```dockerfile
```

-	Layers:
	-	`sha256:572a99d95dba3c7f83700530e7cf60d8f200d4bbb18bd66a193ed91c47b58c32`  
		Last Modified: Fri, 01 May 2026 00:14:06 GMT  
		Size: 7.3 MB (7336887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6b16cdf9d27757a73331de05a765e7aeb816f307af57a7eefb0ad5bbcf00f26`  
		Last Modified: Fri, 01 May 2026 00:14:05 GMT  
		Size: 17.9 KB (17855 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm` - linux; s390x

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

### `clojure:temurin-25-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

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
