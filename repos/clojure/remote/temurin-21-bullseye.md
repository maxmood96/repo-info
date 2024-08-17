## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:f5fdbf47be1f6e0559e86e2627a13617795db13f287f3d535dd6a48084c3406e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:b514fc8d638e7e76a2d09af51a3af0cad7d52473f8db04df4d5b6ba6e753221e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282627588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59632629344a4a9a9c847258f1156d307989578d2ab70a37023816fda7ce98d6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad432ef459ff2d146502cd993dfa5469bcfdbbb62f6f81f8f754484edfa8cd7`  
		Last Modified: Sat, 17 Aug 2024 02:02:34 GMT  
		Size: 158.6 MB (158579249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3be8534da7c26b3dc3cbcb805fc862581dc112154ea5ecdefc1af724885e00`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 69.0 MB (68962624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afcc9e6e275c281833083ad8b3466cabf5603af1be1191b17352edecfcbe255`  
		Last Modified: Sat, 17 Aug 2024 02:02:30 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325d9d1e890ff086b5483f1c5f53663a183a26c635b5a6485423941adb93c623`  
		Last Modified: Sat, 17 Aug 2024 02:02:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0e025616d7c706199ce1570bdaf1e6da40fe15e26552996beb3b85b876bbe70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7057146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f62be96845c63ab904adeb77ac0294f1959baa4c73a2142230d38d68e8e3dc`

```dockerfile
```

-	Layers:
	-	`sha256:de9ddc593ca97678c2384bfe78fbe2b5b89b7e52d534d7b7fda8d3aa2bec713d`  
		Last Modified: Sat, 17 Aug 2024 02:02:32 GMT  
		Size: 7.0 MB (7041030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e743dbc2401a6a6735107bb272cdfa0cd222b42f2b053d11b0668c347b2aef0`  
		Last Modified: Sat, 17 Aug 2024 02:02:29 GMT  
		Size: 16.1 KB (16116 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:85ae8821ff0fda9a2a94d62ceb4069349fa7ebd4830ec7483dc8cc6a7e0ea769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.6 MB (279570749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68c127c5ba6f15431c4213630a6b70035ddc7d0977f90360a2507b2cf88bbc8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad7a41476c1ff4578dc6ea78eddb283c52fcf72abc2d44fd9874b83c9d089f0`  
		Last Modified: Tue, 13 Aug 2024 06:39:30 GMT  
		Size: 156.7 MB (156746174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898b35a2b96fccae41a8a1c82da410f27099dd3a1b4fd307c4a5128a2a662d52`  
		Last Modified: Tue, 13 Aug 2024 06:42:49 GMT  
		Size: 69.1 MB (69093617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5becf8cefd809360d9d9df7b66a8a0f59269e4217ca4593a252933fea86b70b`  
		Last Modified: Tue, 13 Aug 2024 06:42:47 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4a08df0e55d8ad64b7da0f51a8a34166d45215c37e2279346d542aec19b56f`  
		Last Modified: Tue, 13 Aug 2024 06:42:48 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2d314ff7defaa0adb850d6477488db6cb7a56f04f5be82f8eb33535023384828
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7063451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7123bd9d00325387c1b3f06fdc95f8281bf6504618fe00fb994b0864f8931626`

```dockerfile
```

-	Layers:
	-	`sha256:17c1f4dac0adad50aeeba161c4602eb07b05412169f141937427acbbe2590a3a`  
		Last Modified: Tue, 13 Aug 2024 06:42:48 GMT  
		Size: 7.0 MB (7046776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7171529f2a33cfe7159e33d14a0f75daea87288935acf6f3949ebea7169c02ae`  
		Last Modified: Tue, 13 Aug 2024 06:42:49 GMT  
		Size: 16.7 KB (16675 bytes)  
		MIME: application/vnd.in-toto+json
