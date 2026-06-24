## `clojure:temurin-17-tools-deps-1.12.5.1654-bookworm`

```console
$ docker pull clojure@sha256:aff6933713569be6c046a35589c14ef34a0da219c0ffa73fe08ac205f3031169
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

### `clojure:temurin-17-tools-deps-1.12.5.1654-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:3bac6649e0e7cee5d2ce720ab7dae834f3442364f5cc9ee88a98ee777e33920c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272533665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61f34defae16abb861eedf350a32d4a92fb44908e2796693ad833c3b9bc1e036`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:17:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:17:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:17:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:17:56 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:17:56 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:18:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:18:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:18:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:18:10 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:18:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:425befdf76e52426879d2abe42093a00dca59a893e7b4fa2a7679b0180b71d4b`  
		Last Modified: Wed, 24 Jun 2026 00:27:40 GMT  
		Size: 48.5 MB (48502210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc50e56031389fa858a3f35aa0daebd0cbd73820b3f44c4575945a7e6923f4c`  
		Last Modified: Wed, 24 Jun 2026 02:18:33 GMT  
		Size: 145.9 MB (145905427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cd6a08e2e1d6d62722c90fb54d4cff772dc2efb4007b75c37530a2c160c831a`  
		Last Modified: Wed, 24 Jun 2026 02:18:32 GMT  
		Size: 78.1 MB (78124988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cadc8ece6c1931d134c920925c7cc8f570138d907bf1639ee06fe606983832a`  
		Last Modified: Wed, 24 Jun 2026 02:18:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8486c70916201ab12902b23bf3db7fdec9ba8201445f178859ff6b7bee55f67a`  
		Last Modified: Wed, 24 Jun 2026 02:18:29 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a15fbc6b6ad4fc1ad0dafb1b6922f9d4247155a0b0024f275e4d779207b76b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e57a48ddcd0635cad1f9009f24fd89ea20640cf8abb7b9b59001839c8fdcc80`

```dockerfile
```

-	Layers:
	-	`sha256:d4de576948065b6b926a5bf176f83473076d7b3158ef8998cb21e46e9bdb36f2`  
		Last Modified: Wed, 24 Jun 2026 02:18:29 GMT  
		Size: 7.4 MB (7376134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea722844c4ea45ab5249c462ab99f9adcbbe8c60eaf05f0e90fe8234bb138278`  
		Last Modified: Wed, 24 Jun 2026 02:18:29 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1654-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6217c4849a2d9e9598bb4aa7c6ef9f4dbec4794544f6d71999adee4616a7ebe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.2 MB (271244129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83bf33ad1b13be97c91baae1c1f38cd5ba64efcea4f7951ea5d941b5c07d3ee2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:24:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:24:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:24:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:24:15 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:24:15 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:24:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:24:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:24:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:24:30 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:24:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0fb1189398e2e4b474d43aac6502510d0da0318e70137a377c21087f198814db`  
		Last Modified: Wed, 24 Jun 2026 00:27:19 GMT  
		Size: 48.4 MB (48389201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9d82d6d7555817100ec4456b8ef081a1268c7a3cb676ba767e887f3b82db78`  
		Last Modified: Wed, 24 Jun 2026 02:24:55 GMT  
		Size: 144.7 MB (144724321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46bafa5d03598a64c51b88450b56ca54ca76144d05ee36a096aebe229c80e22`  
		Last Modified: Wed, 24 Jun 2026 02:24:54 GMT  
		Size: 78.1 MB (78129568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1741ffcd04c56e75d651902dadefb068df3689b98ae1b223d5abf443a5b1b7d4`  
		Last Modified: Wed, 24 Jun 2026 02:24:50 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6be798f1e09d0b66a8c0cb7e22234b5e5817361d56a593176cc2436c809e79fa`  
		Last Modified: Wed, 24 Jun 2026 02:24:50 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:5f48bcdadf35b78715a37c343dd730380aa9a19ba8cfd6373b02bdd32a612f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc721b441221aea25bb4da2b7aac6df7ccb1d33b75521b173106b1ee99659fda`

```dockerfile
```

-	Layers:
	-	`sha256:c06714521db44756f2847149c1b0bc30b2f8931e4ed50adc310ffa75652ead6b`  
		Last Modified: Wed, 24 Jun 2026 02:24:51 GMT  
		Size: 7.4 MB (7381897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fdbad351caa3ff348137e9ea8f047d7a36dc4f51409b5a4084a22fea9f58e23`  
		Last Modified: Wed, 24 Jun 2026 02:24:50 GMT  
		Size: 16.0 KB (16049 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1654-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:47fbda0f3a54c04af1870cd76ea70baa8145647fbfa89a72327fa59d116ed322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 MB (282072422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171425025726b5c2c164dc9d33b08023025779175217883797f8170b25e5622d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:36:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:36:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:36:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:36:44 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:36:44 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:45:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:46:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:46:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:46:01 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:46:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011a8b1fe08cbca6cfbf84dcf1035227586f8c0a013a520d08ca8f1bb6f1baa7`  
		Last Modified: Fri, 19 Jun 2026 02:40:33 GMT  
		Size: 145.8 MB (145766212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35dfb96b5e9b6425d8814af4e5399cf9c8847f36cf3a1b6f82147a1aadd063a`  
		Last Modified: Fri, 19 Jun 2026 02:46:47 GMT  
		Size: 84.0 MB (83958498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5c5bca98ac641b78dc5411b0899f91406edf1f9c363eedd61e51762bafbb28`  
		Last Modified: Fri, 19 Jun 2026 02:46:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5de3ac346d9b8be5b8fb3a4cb70876d504d56a5b8f675554c3b532dadf8c6d`  
		Last Modified: Fri, 19 Jun 2026 02:46:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a2ee3d925e06a7cb54801dfa6c8d02b849f84b6b07885296e79c2f450745f039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd6c3c51533ed04c1313758db57e9cbfae4dcb45340457304acd9a93af138c3b`

```dockerfile
```

-	Layers:
	-	`sha256:83f9d45b582a7904e57f94b21dc2f88de9cd7cb7f699eb8392bf0a630f10a657`  
		Last Modified: Fri, 19 Jun 2026 02:46:44 GMT  
		Size: 7.4 MB (7381350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b23234a039fa2de838b58936a562683011b490f5995c354c0934c58e6e8299f9`  
		Last Modified: Fri, 19 Jun 2026 02:46:44 GMT  
		Size: 16.0 KB (15978 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.5.1654-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:39979b78ea4002c8014ad104546e816e093f8deac1db81ddf1af1c95e34bae36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (260001970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345236d72888bc80dd836345f0c8f2bee96760c1aece6f6e90a5462016202ad9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:16:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:16:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:16:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:16:23 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:16:23 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:18:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:18:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:18:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:18:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:18:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:467d2d4124b27f04294aa8517fbb889a4ab8a600258034f2ee7ff580572fcc74`  
		Last Modified: Fri, 19 Jun 2026 02:17:55 GMT  
		Size: 135.9 MB (135910421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26c0595dcace2ce17024cccd9ab14acef1227a7fc9d1b390bcfa75a17fc8859`  
		Last Modified: Fri, 19 Jun 2026 02:18:52 GMT  
		Size: 76.9 MB (76929008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a79ef5a24df296b83664eba569d5ed654b9431f805435fd7915420ed616f25`  
		Last Modified: Fri, 19 Jun 2026 02:18:51 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d90918084ed829a6f170952ef3c662216e87d7c51d7bdb8b5c9f0a850e2c66e2`  
		Last Modified: Fri, 19 Jun 2026 02:18:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:71b235417e97f0927530fc34fb4781622134a214bba627fc9836c6c3088e2e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7383385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da7ed18032fdfa8c05d8c34cffe10d9d32cb87aa74a2df92b78c84fe67cefe26`

```dockerfile
```

-	Layers:
	-	`sha256:8fd2796635cc11576b6c80436c16e944d38e08243c760e1bd3447c9f249ee226`  
		Last Modified: Fri, 19 Jun 2026 02:18:51 GMT  
		Size: 7.4 MB (7367453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5d7a77ce0adb86a60044a8d7e449b0e711526c914e515e7b7e8d04d131971c3`  
		Last Modified: Fri, 19 Jun 2026 02:18:51 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json
