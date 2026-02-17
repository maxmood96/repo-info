## `clojure:temurin-25-bookworm-slim`

```console
$ docker pull clojure@sha256:6f19d18235955ed5f1a21591df0feba686c7371b4dd07a11d964df2c6a2d17f5
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

### `clojure:temurin-25-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b0d24c14b4500445e52349d3fffe42d943cc2da1f0223ff3c687206590cb4196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190163340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16b2e69b2fff1f31e9b8d4df3b10b8cbcded8b5c2efa1cc649d8ca4dc627511`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:45:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:45:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:45:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:45:59 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:45:59 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:46:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:46:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:46:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:46:13 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:46:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77437f05fcd5e08c58d99e1215b19a627c3f59f929740a78b912fee96bfd70b2`  
		Last Modified: Tue, 17 Feb 2026 21:46:31 GMT  
		Size: 92.3 MB (92256289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c9d736179f3e1ce1d562c3c21293059ac6fa80effd20fabdb95ae6612e9705`  
		Last Modified: Tue, 17 Feb 2026 21:46:33 GMT  
		Size: 69.7 MB (69677522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c56d06b81a4745d728a06dab5e0d1ec219a4a68cfb43ca3da85588ef839e191`  
		Last Modified: Tue, 17 Feb 2026 21:46:30 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724e5508ec99a79b529d512c1244931a59e8ed68f357ebb7ca268f251b8022e5`  
		Last Modified: Tue, 17 Feb 2026 21:46:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:382e8b1fc91a7822949d1bbf5a46a796e699068f7e2da5af37f1e91bae8c7082
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5099273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d007b826ff076a201888d86106a401ff75e69ed6a84835d169d08b1f2ec8474f`

```dockerfile
```

-	Layers:
	-	`sha256:819ce5e29239982d9a610a80fb3d1f8d4728a0ef95e3fd393c76bc7a5e3e7de9`  
		Last Modified: Tue, 17 Feb 2026 21:46:31 GMT  
		Size: 5.1 MB (5082748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cadbe806933f104c224e5b84bbf342812b5f1b87a7f9abb0b12fe0bc3e0677c7`  
		Last Modified: Tue, 17 Feb 2026 21:46:30 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:31c6fc2d635ce71814dcfaf521e2815984c6b5e5c7f4ffbcca256a12ba8cc567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189069807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d06270ca5d65feed6b39d3d30d0f0fbe9598c7cdc29e12cce9c776b24a6ffe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:45:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:45:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:45:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:45:39 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:45:39 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:45:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:45:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:45:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:45:55 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:45:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4fb92781f5977c953da0ca8bf3803d22f9b891f2250f1fe412965248d48b55`  
		Last Modified: Tue, 17 Feb 2026 21:46:18 GMT  
		Size: 91.3 MB (91288273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb9a8c7ba53d7fb90d177cc883d9ce45c99b773e358d6c10020804fe3ea9bc88`  
		Last Modified: Tue, 17 Feb 2026 21:46:18 GMT  
		Size: 69.7 MB (69672667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95b85146fe8ef105e3e741c5841c460595321565a8e87866fe9a0d51f2e7b99`  
		Last Modified: Tue, 17 Feb 2026 21:46:15 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4eb8037a1c31018a7296e8afaa3a02645f885c846ab7c768f14eb8cd6879deb`  
		Last Modified: Tue, 17 Feb 2026 21:46:15 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:13cdb75b8606ba59094da0ed7ceb4f2f655a97afc8b2e8a8b31f8ba39e705715
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5105197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98111f294406daaee3a4ba254a70783b1a571e7a6fe107a0e0fcd189851e345a`

```dockerfile
```

-	Layers:
	-	`sha256:f2182701e91d70fe112b4c99c794d284fa5bb728afa0b1b143a101cc318fe23b`  
		Last Modified: Tue, 17 Feb 2026 21:46:15 GMT  
		Size: 5.1 MB (5088530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceda88d4e71ebb99e88bfeabc454dc31920aeb8b9b9c29449e0fa0346e7b8968`  
		Last Modified: Tue, 17 Feb 2026 21:46:14 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:83c8eda2a3cf3f6cba32328702fad5059475c851779134c3400873d22213d90d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199216822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43fc958b58d01acd7176e51f6ab2352e48f6ee5282ac77174baff581b6619cf7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Fri, 06 Feb 2026 00:46:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:46:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:46:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:46:09 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:46:10 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:51:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:51:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:51:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:51:16 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:51:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91cb234547828975d01511eb3f1e2f07f4c3226976323dbaf0a3fe8832f8431`  
		Last Modified: Fri, 06 Feb 2026 00:47:43 GMT  
		Size: 91.6 MB (91632917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7d1bff7a7aa17d12bfad8d52d8030be45d899e876e5cf39f0f2c8d9fcfde89`  
		Last Modified: Fri, 06 Feb 2026 00:51:59 GMT  
		Size: 75.5 MB (75514150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feea98bb1e6e49d6287c83e30989b16ea90787b12d2ccf31792e8ce47337c41f`  
		Last Modified: Fri, 06 Feb 2026 00:51:57 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f3e6a206e0bf371d7ecce2d701cc3627bcb799a2f65be0b2b875a0a201c6cd`  
		Last Modified: Fri, 06 Feb 2026 00:51:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b6c0830e1dca1578d0a01f0229f1fcce10ca4d151a5e887bfa3d018ebc8b8c06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2093db5e1b39899cb91fa4a744553f1cdaddb5d215735b0083ad5fb6cb93f236`

```dockerfile
```

-	Layers:
	-	`sha256:ae6cde9575c74875a271958450551dc22c10e3a261966655652c29e78440edf2`  
		Last Modified: Fri, 06 Feb 2026 00:51:57 GMT  
		Size: 5.1 MB (5071230 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77072055f2f3d6006a364706329fac99df8a7d288c7a6af1a1245872ea7e8840`  
		Last Modified: Fri, 06 Feb 2026 00:51:57 GMT  
		Size: 16.6 KB (16584 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:5fbb175a189882c3caf62e57e6917acd11bc2dd955dcadfa599e023d505ccf0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183609108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d818e0411f4af3afe3c851d59b45ff7bc3bbacd76020f715d1969db669d1ff0f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Thu, 05 Feb 2026 23:09:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:09:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:09:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:09:41 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:09:41 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:09:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:09:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:09:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:09:55 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:09:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6189fee1a38e1d1dee751bc8f3d8e5e91fe8fbc5d67b44beaa51e99ba08aa5f8`  
		Last Modified: Thu, 05 Feb 2026 23:10:22 GMT  
		Size: 88.2 MB (88233820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cf95a8e28abc364d5bdd4bd71f6d589afa687e7730b29e8585c87094a96d72`  
		Last Modified: Thu, 05 Feb 2026 23:10:22 GMT  
		Size: 68.5 MB (68489860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc727604941f1a22fe52b9f2e6cf82126c2a0882fa15868b56a02b819eae3b53`  
		Last Modified: Thu, 05 Feb 2026 23:10:20 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:515ac85dd50a50b4ce3946a61b20127660e1bdb4691b4c40d68596e0077d8706`  
		Last Modified: Thu, 05 Feb 2026 23:10:20 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:899f3aade18d94fa0d2c9bedd9608b44171bfd01520d568795267fca8042ead0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5075154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1090f20d039f088668f6a6560e8e017476f91753dd32a9cb2a7bcc0e4becbddd`

```dockerfile
```

-	Layers:
	-	`sha256:c186fe6a5d85db5d3e7648fcf8b249ff4bb26e1e671d40ff5159003bf699e457`  
		Last Modified: Thu, 05 Feb 2026 23:10:20 GMT  
		Size: 5.1 MB (5058631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab543f7d36e22564037401796f5af692965e3306d8018098e006979f03a1691f`  
		Last Modified: Thu, 05 Feb 2026 23:10:20 GMT  
		Size: 16.5 KB (16523 bytes)  
		MIME: application/vnd.in-toto+json
