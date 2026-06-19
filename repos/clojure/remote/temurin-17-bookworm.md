## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:2710a30e8a1a6641dd7f8adde37d1bec60942949b1d1700e6feaa64b9afca49d
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

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:8f0b2d11d19ea759f36b51509e4fcf1842af46dc5570366cdfe2a716aa47199c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272533453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2216ddc05c417ceb5f486898756e84349fefcc2643887e0cae6149fc09ff24`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:17:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:17:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:17:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:17:10 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:17:10 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:17:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:17:23 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:17:23 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:17:23 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:17:23 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e4c3e476177eb9585360b2cc1674d41d015ca701d0d28d440edd435445fca7`  
		Last Modified: Fri, 19 Jun 2026 02:17:45 GMT  
		Size: 145.9 MB (145905415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8365cdfe7f7c1c1983ddd88c2f8916d4cad0219767320a40c80abce8715789bb`  
		Last Modified: Fri, 19 Jun 2026 02:17:43 GMT  
		Size: 78.1 MB (78124956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25e05b657b7fb0d0bbb88d86a7f347afa6d1c7f4c0015bce784533926a621d7`  
		Last Modified: Fri, 19 Jun 2026 02:17:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842b38196b8e649d35dcb2cc07973916151c86704c14f8f9a190cd57132e7d9d`  
		Last Modified: Fri, 19 Jun 2026 02:17:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:a93e830c3a94ed45ed29eea9a9fbcc80e73b98fa87bacc7d4ae873eb71088505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4639f9ae0874dbd4c2494ac1b67fe426d56ffaa21ba7cca7607c68c9281830b`

```dockerfile
```

-	Layers:
	-	`sha256:39308e129e288ce53eb4b00c3c9d5ff32267b628cd4e4349f56f6d49f7cfe2e5`  
		Last Modified: Fri, 19 Jun 2026 02:17:41 GMT  
		Size: 7.4 MB (7376134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a9f2e30e0ec8ca6a904f3e91f9cbc76e3244327a44875c575ccc897dec5cd3d`  
		Last Modified: Fri, 19 Jun 2026 02:17:40 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:89dbae63de8a5fd581a28b22e9a5839995e53408147918b31e413af2fe9517f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.2 MB (271244055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75e88d13f30d2bb4232aa6519eceb8401612a43dfe78e3e5549ea33d75c8ab17`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:17:30 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:17:30 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:17:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:17:30 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:17:30 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:17:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:17:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:17:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:17:44 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:17:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cb297dbf84a696602e8a57a7bd279ba0131a6e3c9875a73976afe75ad677fde`  
		Last Modified: Fri, 19 Jun 2026 02:18:07 GMT  
		Size: 144.7 MB (144724310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1211494eee234e6731dc22ce5ba4c8c2f6b3fbb6cf4078136894b890c3ae635e`  
		Last Modified: Fri, 19 Jun 2026 02:18:06 GMT  
		Size: 78.1 MB (78129688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4785564b48694542ead5eb05b6b4d304067dcc75745993157b60e81d9618553`  
		Last Modified: Fri, 19 Jun 2026 02:18:03 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4da46ab6adb676ccceb8f75a377018be8185f12fa0c6edcb49ec6933f58d6c`  
		Last Modified: Fri, 19 Jun 2026 02:18:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e38523ed166ee0daff4ff0795c08c849506593388a3ff922769882b1c0db9cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98a554e0603e772c8416f7fe68340216c66b761e0087b0f19ec209b428bfcb9`

```dockerfile
```

-	Layers:
	-	`sha256:577fdc0cd43c6aa3710746514b7c17b9fc4eea6a8c6003f70043752145b58bcf`  
		Last Modified: Fri, 19 Jun 2026 02:18:03 GMT  
		Size: 7.4 MB (7381897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31fe693175afb316bebe44caecc199337158413186f88c9c4c16f0b104c1b6df`  
		Last Modified: Fri, 19 Jun 2026 02:18:03 GMT  
		Size: 16.0 KB (16049 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; ppc64le

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

### `clojure:temurin-17-bookworm` - unknown; unknown

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

### `clojure:temurin-17-bookworm` - linux; s390x

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

### `clojure:temurin-17-bookworm` - unknown; unknown

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
