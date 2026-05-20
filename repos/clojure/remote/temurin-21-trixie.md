## `clojure:temurin-21-trixie`

```console
$ docker pull clojure@sha256:a97cf6b75b8719cab188b99c0d561392e76d6ce9d8b633217cb19122d2b1d0b5
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

### `clojure:temurin-21-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:c52e29ce2b522458f27a683fbe82c0e8cae8f7a7a95707b1078577fcc82010d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.1 MB (293086032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee409dd18028e99a1ec945ecaf72fa76ba6e6cb7823fe2a47c581b2f24ab52d6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:00:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:00:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:00:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:00:26 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:00:26 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:00:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:00:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:00:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:00:41 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:00:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72682a19132331125da4e556b730286c47e80716c17c1f2a759b795727a3f213`  
		Last Modified: Wed, 20 May 2026 00:01:05 GMT  
		Size: 158.2 MB (158166903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ad5350e78395575fedd06a7ba1078ac1d966a8d14166cc2fda813d20352cf6`  
		Last Modified: Wed, 20 May 2026 00:01:05 GMT  
		Size: 85.6 MB (85607466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9224ae231ed2db838c5904b10500b70d680628b5558ac8c395dc497d4de842`  
		Last Modified: Wed, 20 May 2026 00:01:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22aee13c8b13c1bbf8975ab11ebdd94d407534ec0842e1e6ff9651810d95f567`  
		Last Modified: Wed, 20 May 2026 00:01:01 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:aa673727a91f1cb468762171dd718b56ae95c09138fe9cf1868194ea126ca549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4ddeaf7e4d0b0e8ed661d18069d1f10931176acc113ffd2a565aaf823548e4`

```dockerfile
```

-	Layers:
	-	`sha256:c70fced4db80473d9726436e24c161a51332ea7e9775263c4beef9c1c94cf11a`  
		Last Modified: Wed, 20 May 2026 00:01:01 GMT  
		Size: 7.5 MB (7473348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66b7d3b796cff1cde0f015c603d4b1d3461e54492dde0b6ee9f1da24a791f347`  
		Last Modified: Wed, 20 May 2026 00:01:00 GMT  
		Size: 15.9 KB (15907 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d237494d98edbf9b7634a174e9248d43364e67c5a3efccc2c4b3b86dd557008f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.6 MB (291566538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcc727da178b179bd87d8af1f59f39a1b0e1369b1861203e7163867005562d7f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:07:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:07:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:07:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:07:19 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:07:19 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:07:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:07:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:07:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:07:37 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:07:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cb1082863d9cd40aa2629c95c556c8a61e16ac11388c1537c1852fced36445`  
		Last Modified: Wed, 20 May 2026 00:08:02 GMT  
		Size: 156.5 MB (156461324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1f489074a274556107e92ffd428682b28329159ea3372555b75851d9092486`  
		Last Modified: Wed, 20 May 2026 00:08:01 GMT  
		Size: 85.4 MB (85431952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f34972dd3de03634f1c4747cb6ad556a3e7627022a45628db4fda3e4186fa5`  
		Last Modified: Wed, 20 May 2026 00:07:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caddc4c49f7be036bc9e0dab595d92816836eea0223cd7a3990c3b954a4cca3b`  
		Last Modified: Wed, 20 May 2026 00:07:57 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c446468f46233fce857d27b94dedfcccc801328f7a27f5526ac229bef7e71200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7495767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fbd3f9c6b5fb566c32024db68492ba22e3e420cef7d2f62087bf5598cd24603`

```dockerfile
```

-	Layers:
	-	`sha256:c3775f7f1dc85c497daf43225c2adb6cb834de83da34fbbc43063f66bee7ad72`  
		Last Modified: Wed, 20 May 2026 00:07:58 GMT  
		Size: 7.5 MB (7479741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be8c67b03a0f561a2f8d253e9a84c8d558e1904630ecc659216c5c628175fe3b`  
		Last Modified: Wed, 20 May 2026 00:07:58 GMT  
		Size: 16.0 KB (16026 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:013f1fae93db27e695a6f03304ec5bed803c58c910f00e639eac22ec4da7c834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.5 MB (302503805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc3dc26f55cc408b7bf75af95c51994b3e669bee401399c31b9a8b6483951c09`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 06:02:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 06:02:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 06:02:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 06:02:25 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 06:02:25 GMT
WORKDIR /tmp
# Wed, 20 May 2026 06:04:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 06:04:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 06:04:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 06:04:33 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 06:04:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b629dc606e724e659e7094cdede449bd2fe74e4594977f7749e2b2b2395027`  
		Last Modified: Wed, 20 May 2026 06:03:43 GMT  
		Size: 158.3 MB (158343282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244e0cf2c59841725e0b9c72c2bb0d8bba5af36574ccfbad81ec8c1f20a60dc7`  
		Last Modified: Wed, 20 May 2026 06:05:14 GMT  
		Size: 91.0 MB (91027300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2392fddcc3aa110a1f9c91c2f06d9ab530786060c217776ba7741828b35bf10`  
		Last Modified: Wed, 20 May 2026 06:05:11 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f495592dfd4ab403ad0e1ca3eb719745e7369caf4f0910673fae8e87df7159a`  
		Last Modified: Wed, 20 May 2026 06:05:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:19c0fab9fbef98c2ecada590dfdd3ad864526d09b6b95c6838da2d8eabb48e74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe2d435fdc4635311f3f5b524cab11c13834549af348d85c16561abe078aba7`

```dockerfile
```

-	Layers:
	-	`sha256:32c080685653d9c5b7c571f29dad7751ac9abc00768248080f51d7754c3325c8`  
		Last Modified: Wed, 20 May 2026 06:05:11 GMT  
		Size: 7.5 MB (7477769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2da7b197cfff6292b9ed57ba3355551d3f0ef0426b86781c43be62944fe1690a`  
		Last Modified: Wed, 20 May 2026 06:05:11 GMT  
		Size: 16.0 KB (15956 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:a3e4a28c2c8e565aa8e1b2be248e57826ffc8cc98e8fb0df3d272715508fd47c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.4 MB (283359947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d537166cc0a791d0151a292585585304bcf6605b799ef4a15b148d779de984`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:51:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:51:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:51:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:51:09 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 01:51:09 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:51:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 01:51:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 01:51:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:51:25 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:51:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1540dbb0587ae9097c9d04c50809503aa74d42814940d640c6659645acc0bc6c`  
		Last Modified: Tue, 19 May 2026 22:37:00 GMT  
		Size: 49.4 MB (49379780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b3fd805dcc7ba668e43c67f4286fb90b6ee696b4a4d5021b06999d31fdc087`  
		Last Modified: Wed, 20 May 2026 01:51:58 GMT  
		Size: 147.4 MB (147388366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a1e4e91055bb72e507cd886f6e2ba28bc604ba0f7ecf8d7490be155576b0eb`  
		Last Modified: Wed, 20 May 2026 01:51:57 GMT  
		Size: 86.6 MB (86590761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae6c5ca3c2623b51ef7ef8046983f249df9274fae771a7fc2a2c57efbb24d21`  
		Last Modified: Wed, 20 May 2026 01:51:55 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a779c9c2bb01dd187afa5d9d94488f029066dd5a39d7facbb4128d74e28d2ea`  
		Last Modified: Wed, 20 May 2026 01:51:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:98da343de6d975c0340f304f36e28dcd40878966169d8518a98013a439f83798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7485177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9b397c182f48e0aa29a08a092265b377da022c812c84b605f14cee03b8a3e21`

```dockerfile
```

-	Layers:
	-	`sha256:4455a9f3a64e79db46ebc4867efc9e14096ad21d98ec890d243952e46fe594e7`  
		Last Modified: Wed, 20 May 2026 01:51:55 GMT  
		Size: 7.5 MB (7469270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab59677ba23f31c3f18ee9357fe321880fb2cd1662d6ab381f34f1ea05f029e8`  
		Last Modified: Wed, 20 May 2026 01:51:55 GMT  
		Size: 15.9 KB (15907 bytes)  
		MIME: application/vnd.in-toto+json
