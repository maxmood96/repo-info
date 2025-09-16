## `clojure:temurin-24-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:aafc41e825793127cae2fa1c051fb611f004db585d5cf60f65bd8717abbf3957
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

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bb9119111fc2a62d936a019ae01c4c1acf4846dadbdc4d32d6936d74f2f7e4e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187874055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:febf2499283420752bac393829fb3a319ca5b942143679e0e1f43ee439e7a87c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d107e437f7299a0db6425d4e37f44fa779f7917ecc8daf1e87128ee91b9ed3d3`  
		Last Modified: Mon, 08 Sep 2025 21:12:45 GMT  
		Size: 28.2 MB (28228346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952d824fa62fafca1c35900887ec16fd6238d531702356825c9029d1c2586510`  
		Last Modified: Tue, 16 Sep 2025 00:22:10 GMT  
		Size: 90.0 MB (89975206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e483e2945f9eef54d3c0f2f9d3b41b53ee6721a810841f2078b0091c31ac93`  
		Last Modified: Tue, 16 Sep 2025 00:22:09 GMT  
		Size: 69.7 MB (69669458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a565f65616242b5abfe9d875ccd898608e2742b030150567b6f38b9ce6e4a076`  
		Last Modified: Tue, 16 Sep 2025 00:14:17 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:272ae95c2c48982deee0b55dd04b478475f1d7abb6b16adc6a163274c87d1519`  
		Last Modified: Tue, 16 Sep 2025 00:14:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a376da7e600517c00e3090ada7f49033e0bb98f67a0b3c74511166a92030f8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5079908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89554350cf0a854cd568b0d1b0c5d5cb17f412f7bf76ea93847cdc5381848515`

```dockerfile
```

-	Layers:
	-	`sha256:265ebf14a337e1c6d828c47dc6a0d2d0466fa4d1b580c7fe4692148b3736ec04`  
		Last Modified: Tue, 16 Sep 2025 00:44:35 GMT  
		Size: 5.1 MB (5064036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85b867498f3c81253b6a23b86a7371897a6f3cf72c0f560ad518e33d151fcfcf`  
		Last Modified: Tue, 16 Sep 2025 00:44:36 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b000d03abd5adead486f9d64da96020bc8cb508c3017c7b0d79d299f816e8381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.8 MB (186754768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac52c446a0d6a77d3d6a623c4234b64609d02f218ba89a1615b3a4ac4427c517`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0878ecc8b0afd0d835641c015541aacd4780ec19e5565a3e1a5af3f77d208d42`  
		Last Modified: Mon, 08 Sep 2025 21:13:25 GMT  
		Size: 28.1 MB (28102099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d2a03efeeba1e158a24d85add18acef28b55a0b55fe230dac3317d21e802f1`  
		Last Modified: Tue, 16 Sep 2025 00:36:04 GMT  
		Size: 89.1 MB (89092475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eccb4077e45e3b7a3770f4c2b0702d8621844da36906d97ac47941fa25f3c2e`  
		Last Modified: Tue, 16 Sep 2025 00:36:02 GMT  
		Size: 69.6 MB (69559156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1676ebbb419908c9804e1570d3f2d7ae5e0d3ef08eeb5e26a8d0b07860b2dd`  
		Last Modified: Mon, 15 Sep 2025 23:35:06 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2318792cd6cf7527c6ca8c0ea6b8629f47a982b93983aa15f12998acc8a93204`  
		Last Modified: Mon, 15 Sep 2025 23:35:09 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:170511c18efa0884125bf77cf847cb51d3ca51e2043f3e0609553574531a8901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5085784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cb6a0bbfd5a7bf110ef814a4c41fbcb7a8eeea241a85383cd602f204421e440`

```dockerfile
```

-	Layers:
	-	`sha256:352d02bf95aa10149c8b50e8d16390d78278bf1a6b3eb28fcd26454ca1481e40`  
		Last Modified: Tue, 16 Sep 2025 00:44:41 GMT  
		Size: 5.1 MB (5069794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf9fa39c91c22c81d90f06ad8a5be88aea162d307915060928541890a634bea1`  
		Last Modified: Tue, 16 Sep 2025 00:44:41 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:70d24fcf4eea2db10bdbfb222c562d3f2b2d737996f40b68af460298236516af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.5 MB (197498692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da846bf06b09760f564b505ebc4b8dd0d4daaf9233f97b9b4e06567bfff71bb2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a438293490bbc2af66661166949a4d86358eeb39f9fadd5b0146666f05b9b9ac`  
		Last Modified: Mon, 08 Sep 2025 21:30:47 GMT  
		Size: 32.1 MB (32068762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fd09d5192cc7e3cbe99d4d308da8fdfddb81b3944db144f97d3a1682452e5f`  
		Last Modified: Sat, 13 Sep 2025 03:51:41 GMT  
		Size: 89.9 MB (89918193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca3d037a96879bba09b61ca11e29167c500c003a31bd6e5e207ed6355f3fcb6`  
		Last Modified: Tue, 16 Sep 2025 01:32:49 GMT  
		Size: 75.5 MB (75510695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc0a75a8ce60c7dec2491165b0838791edcc87da0da8a087ce6e8d9aad7152c`  
		Last Modified: Tue, 16 Sep 2025 01:32:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576c75b3ceb0b12b24db1444b79187f200d530b6539e60b2c52912e19fb69195`  
		Last Modified: Tue, 16 Sep 2025 01:32:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a9296d8d05048f5fb552304ba2097067a3bbd89d350984ba2522c39f7d238945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5086411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a0080ccab0be957f59899d59fe1db286929b8549e4be4ec38d6b491e4028287`

```dockerfile
```

-	Layers:
	-	`sha256:c97f5e8252e82bd73f7cd10cd706cdb1ba55a670c5453b912164d324e23be700`  
		Last Modified: Tue, 16 Sep 2025 03:42:33 GMT  
		Size: 5.1 MB (5070492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0dfa0174522692bf592860f7a08683e43ec885ecf750abbfe03e9b080e40fe9e`  
		Last Modified: Tue, 16 Sep 2025 03:42:34 GMT  
		Size: 15.9 KB (15919 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:ad18330d3585bfba0959372854bfda39995026257998395b430cf2b1bcafec9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180597239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e5d581425ebc57409eb23610b847a32d9b48565b86b9aeb93e9d7e4b9ab153f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c235ccf5178d9b6baa6b3965b50fd208e8804504a8dff76fd257b0d061d8dc10`  
		Last Modified: Mon, 08 Sep 2025 21:30:55 GMT  
		Size: 26.9 MB (26884297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8062d35212474884f57e135a7c513bcb3237247281dcb5972254c07f21343289`  
		Last Modified: Sat, 13 Sep 2025 03:18:48 GMT  
		Size: 85.2 MB (85226409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e1352a10f238f371661fffa02d721dcf2d996e44fca45d7a5b55c2e8fe257a8`  
		Last Modified: Tue, 16 Sep 2025 01:03:51 GMT  
		Size: 68.5 MB (68485488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29a76b375c796661fa9a46b67a79fdee6726946b789446987e671ab717ce775`  
		Last Modified: Tue, 16 Sep 2025 01:03:46 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8a9eee6130d6e095ba7c741b4b9751fc3fd2b02e4b2cedee461df8e3e4a0bc6`  
		Last Modified: Tue, 16 Sep 2025 01:03:46 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ee5b0dccb6c2b77d1971fc4017d421a86ed5b0b39dc0d210534c84f97a9081ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5073777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1591f3a6e3ae9fb09c387e7f8e20cf3d20c2ea79f3c6299c7e39a109d3a73d9e`

```dockerfile
```

-	Layers:
	-	`sha256:8b14395ef15663f6a2492359ef3a87aa390bc6de72754756f5269cbdb1d249ae`  
		Last Modified: Tue, 16 Sep 2025 03:42:39 GMT  
		Size: 5.1 MB (5057905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d745788f28b65e55115d63426d7bf8b8a0933d400e284f231cdf684798afaa63`  
		Last Modified: Tue, 16 Sep 2025 03:42:40 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json
