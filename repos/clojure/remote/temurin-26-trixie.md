## `clojure:temurin-26-trixie`

```console
$ docker pull clojure@sha256:e368320b0d3a694f9e83cc5fb92a35114773d36501835b49f1b292a03303d62d
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

### `clojure:temurin-26-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:a69886d52099936e3abf2b0ffbeb74bef9be8370d20b67f27ba464c0ca5775e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226353424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa90563a7516780939a47e8f88a9579c5a7cf04c0de4a3e1e32854fe8284377`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:48:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:48:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:48:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:48:10 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:48:10 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:48:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:48:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:48:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:48:26 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:48:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1733636883040f3f18e6f93c56d1509e5cf1af1a420bef5a315d5b1c6be5847d`  
		Last Modified: Thu, 04 Jun 2026 17:48:48 GMT  
		Size: 94.5 MB (94524332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e33e68976ac209c3360c9b534b9e4b7b4b676c7c0108d595867029f8017140`  
		Last Modified: Thu, 04 Jun 2026 17:48:47 GMT  
		Size: 82.5 MB (82517429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d7fd300d928361025cb4dd6d7d2b3143906682e7b7258d0c9ffea2fbea9c60`  
		Last Modified: Thu, 04 Jun 2026 17:48:43 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3c229dc9f1d5e7f6d5efa3108e11b4e244ecb2bcad144f1e816815b36ba3a9`  
		Last Modified: Thu, 04 Jun 2026 17:48:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:316f3377b7293354d34547b3dbfe4aeae7f58d1186937a8f9df9bd7c5f30b32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7449563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e6b6ac8948a56f1d23638c1cd5d2c5e7e5749858a2ae7742ef8c6dc2f6fdb96`

```dockerfile
```

-	Layers:
	-	`sha256:e6b80a9d6b31cf2beb34b0a31b7a5c224069694493007d7fd1967c7af2530358`  
		Last Modified: Thu, 04 Jun 2026 17:48:44 GMT  
		Size: 7.4 MB (7433662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:139707ab90ec0f17ee7430241619e5229ef88325e4a04208cd9f1565c4599c10`  
		Last Modified: Thu, 04 Jun 2026 17:48:44 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a584083bf9a0a005d770de81ec5a19f5f73343bc6067cf8ae154f100ee5f0cc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.5 MB (225515793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd264b62eeacce56b0c3fc84b7887ee0723ee8bba50575974534302c4afda44`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:48:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:48:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:48:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:48:04 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:48:04 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:48:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:48:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:48:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:48:21 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:48:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abbd4d754e84a46eabceda079e5a75f11bbcf7674144bebfe8751dc8270c861`  
		Last Modified: Thu, 04 Jun 2026 17:48:44 GMT  
		Size: 93.5 MB (93504334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d139b8f4a2718da4ed03c83a1227b7c4199512becd297a23ccc5b5f018e3e1`  
		Last Modified: Thu, 04 Jun 2026 17:48:44 GMT  
		Size: 82.3 MB (82338201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2decb0f0974e4b1732120336fa1cf50c7223febb058bf73e0d9f62f8bbb2db28`  
		Last Modified: Thu, 04 Jun 2026 17:48:41 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6698380491bc6c5a6f287f60f5783caec9852eea16bc6cab8efdbe9655c591`  
		Last Modified: Thu, 04 Jun 2026 17:48:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:664094c95473ca6461c48cceb87b5c87db53f48b8709e685491779b91061c8f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7456071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a05d33d1520942c561b7a2f7a25da73cd5ce586b41249b220cb53d762bdac27`

```dockerfile
```

-	Layers:
	-	`sha256:afab4c0b7479682d0129da14968788b2718b2227f7f7b3b7222dcc4a7310b2de`  
		Last Modified: Thu, 04 Jun 2026 17:48:41 GMT  
		Size: 7.4 MB (7440052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c03bfc360f13bbd1dfeab56a9d280630007db4960c8c1a509654169dbe8060c3`  
		Last Modified: Thu, 04 Jun 2026 17:48:41 GMT  
		Size: 16.0 KB (16019 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:ac500104ced796040f991b5ba712f63d294c52ce1eb2513a3bd1af28a89eb415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.0 MB (234973488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfa9e070b9b06138be788576113dfb5ee57c644162a33066095914155d66114a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 18:11:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 18:11:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 18:11:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 18:11:25 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 18:11:26 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 18:12:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 18:12:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 18:12:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 18:12:12 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 18:12:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d4e5a75672764ebd26ebb0de7d78defd969db6824877814166a298385cb200`  
		Last Modified: Thu, 04 Jun 2026 18:12:55 GMT  
		Size: 93.9 MB (93902050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291ae22018110ab9bce3bb8813caf4eee8feb3c2c48bd1f54e979489cb436c8b`  
		Last Modified: Thu, 04 Jun 2026 18:12:55 GMT  
		Size: 87.9 MB (87938213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab5ea81211e2241017d3225c63fb61be8d8a1754612f9ff8655da04e823cbb8`  
		Last Modified: Thu, 04 Jun 2026 18:12:51 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc91a3f95ba8c0ec2fc60a9dbf98bc2a5200c2a32ee85914e9769e967dce6698`  
		Last Modified: Thu, 04 Jun 2026 18:12:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a4c154ad51c094f69967716e626f84275683a8e6d43469f3e2a49f9dc274b6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7437968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f17b755c8ce51aac546db7827e7009f7ab020cf04428fef2e772b55f74f9781`

```dockerfile
```

-	Layers:
	-	`sha256:c0adb965c84ce5cf5e6a0a702220227d8446768a4860e6de4c6c952504f205fe`  
		Last Modified: Thu, 04 Jun 2026 18:12:51 GMT  
		Size: 7.4 MB (7422019 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f538b178919a9db2c3e8575fa09827dfaf424778b36748b61b899a14855dd9f`  
		Last Modified: Thu, 04 Jun 2026 18:12:50 GMT  
		Size: 15.9 KB (15949 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:3cb8919a93a8a60260b839935b7936356ec48403aac0f1574d74eba27376336a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223419576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab13e48008da68626693a49c215a47dd8d8746406b621d50dd6e7943231f1d04`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Thu, 04 Jun 2026 17:47:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:47:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:47:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:47:41 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:47:41 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:47:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:47:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:47:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:47:58 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:47:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1540dbb0587ae9097c9d04c50809503aa74d42814940d640c6659645acc0bc6c`  
		Last Modified: Tue, 19 May 2026 22:37:00 GMT  
		Size: 49.4 MB (49379780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c640a847493e3a6f59c7b68e4eefb714a110a3d05f22b8280068369b93250ad8`  
		Last Modified: Thu, 04 Jun 2026 17:48:32 GMT  
		Size: 90.5 MB (90536985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffd8449ec9f427de7f88c257dc31682ed6479908618c047b5e1840087fa3a14`  
		Last Modified: Thu, 04 Jun 2026 17:48:32 GMT  
		Size: 83.5 MB (83501766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83b011bbf8e65c7872266c82a3c9e539d5a2fd93d92c2ffcd8c37cb01aca592`  
		Last Modified: Thu, 04 Jun 2026 17:48:29 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb741ae076984575ade858ccf9758887828418f4087b6e96285a8aa9dd3aadeb`  
		Last Modified: Thu, 04 Jun 2026 17:48:29 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a96e77ea3b66c929334a61ced71cd04bfc185293d395b2ddd3ab499b276c1eaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7430671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd87b7c2d2b8fe8ce2acf39e827a446dde6274dfdf4d588eea3dc90c2e714ea5`

```dockerfile
```

-	Layers:
	-	`sha256:22e7c9cae1ec957625d85a0f2253a06bb432527579d85f6253c871a968f389a7`  
		Last Modified: Thu, 04 Jun 2026 17:48:29 GMT  
		Size: 7.4 MB (7414770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d827139db0f8fe591adc51e8a376583e25280cc5d3d77ca8b79ade33b9fced5`  
		Last Modified: Thu, 04 Jun 2026 17:48:28 GMT  
		Size: 15.9 KB (15901 bytes)  
		MIME: application/vnd.in-toto+json
