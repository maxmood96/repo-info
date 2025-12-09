## `clojure:temurin-8-tools-deps-trixie`

```console
$ docker pull clojure@sha256:8eebb9be6996e27eaa0eae2b389cc47f765bc7d60399920a4beb2f4845854116
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:87dc459a2ee931fcdaefb8d5b4ef3c375c97f1929cb1efcfb2cc70af9cda99fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189564459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253900735460dc6ab4aa0bb288e78abe32ffac7d4a10e0daab2efd572d03e249`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:50:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:50:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:50:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:50:24 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:50:24 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:50:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:50:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:50:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb392fcd0bced9416ef81d8e77a3db0723a27c44865790b81df81caa8ee115b`  
		Last Modified: Mon, 08 Dec 2025 23:51:11 GMT  
		Size: 54.7 MB (54733371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e21fcf91ddf65d277d86da7cdb2b6d65513305d23d65566d822a803f38c035c`  
		Last Modified: Mon, 08 Dec 2025 23:51:14 GMT  
		Size: 85.5 MB (85540925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422d3ca6c57641e7fca7aca224a43893a55995b24e7a28da7b8ac8a7cf170dc1`  
		Last Modified: Mon, 08 Dec 2025 23:51:05 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2f280254bcc713669efa8f5992bea578e68fe1c46455d660981be63ea0f8d97b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7262f7c6471ce419550e7ff5bb1328dac225ad8dca23ac2da5d2d62d6a2c0efc`

```dockerfile
```

-	Layers:
	-	`sha256:2e75b7750f669cabc0223eddef0d7f837ca0aab18b72ea3548be74b7ad59c45c`  
		Last Modified: Tue, 09 Dec 2025 01:40:28 GMT  
		Size: 7.6 MB (7588539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b07d48bb0383ad7cbbc35c3cd699a319bebfc03fd7837198a90a955f3aa8215`  
		Last Modified: Tue, 09 Dec 2025 01:40:29 GMT  
		Size: 14.2 KB (14170 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:066c2940b02e928932a71acfeafacf609f981c8d50e05a23ae6af813887f6aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188830329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c505498f855130f9a02526b4972fe0cf38020add324a31564396c127c9ff14`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:58:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:58:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:58:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:58:50 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:58:50 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:59:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:59:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:59:09 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:504e105dc4a53396c195f96c4d53355691233de14616d93dfc3ff1761e98cbd9`  
		Last Modified: Mon, 08 Dec 2025 23:59:42 GMT  
		Size: 53.8 MB (53814993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe039b59ad7776f032f4e4c2bc197c8b7120c6facca5a9e592853b3737a5789`  
		Last Modified: Mon, 08 Dec 2025 23:59:45 GMT  
		Size: 85.4 MB (85364466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ee9211fd35ea37e710000366e91f9277ed65529cd2b8c9ec73010115c16c4a`  
		Last Modified: Mon, 08 Dec 2025 23:59:34 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8deb12655022d5009f29c443b5f6aadcad5170e5afdde75e6c67733b0a0b323a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:882d33820a5f9066324fe46696805d1e39a1527adc19388959319be9adcf10ea`

```dockerfile
```

-	Layers:
	-	`sha256:8955019679239a7c83ce5a664ae3f981ed0c0ca6f024e6dfe56ee6f53121fdea`  
		Last Modified: Tue, 09 Dec 2025 04:49:40 GMT  
		Size: 7.6 MB (7596267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a61fcb18c0f2de98742907664c3b5b172d9442efcb3e9be5034ad05bc756808d`  
		Last Modified: Tue, 09 Dec 2025 04:49:41 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:3d7c652380bcb790ec1e0d1e6fe10a1f2d510726501c3d0f0af936e455d340e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196231755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e2bd645c8132afed74a78a94bf3e5d437d9ebd3496fdedf880e9fbb097e87a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:23:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:23:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:23:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:23:38 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:23:39 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:24:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:24:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:24:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fdcbbf285191165c95df89028a64259c84d1fd6873060f7cabecc5d7fc9547`  
		Last Modified: Mon, 08 Dec 2025 23:25:07 GMT  
		Size: 52.2 MB (52175122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891082bb1e05c9f765795b20d511d6918e35d2c66b3fa35cac6d0cf82f2f621b`  
		Last Modified: Mon, 08 Dec 2025 23:25:34 GMT  
		Size: 90.9 MB (90947510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c51f681687c5faef873c158dec7b49022fd212fd741588e52c23e5f7a6d6fcf`  
		Last Modified: Mon, 08 Dec 2025 23:25:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a7f89413e7061312579462d8852a9e21765411efe397cbe55cd6b6d21bd8dc29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7607769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c716a2729ff4409086fa5678b3ae1740cc919e1a7a145391a8baebd8563202`

```dockerfile
```

-	Layers:
	-	`sha256:b29ac7da0ce764f7d575cf00cfb8ab1c5f3291b386fe2c427107aad6bbdc9fb2`  
		Last Modified: Tue, 09 Dec 2025 01:40:42 GMT  
		Size: 7.6 MB (7593551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fe46faca7a03720b687c1aa8996b90446cae1a0cbb9e970118c4416f30332a0`  
		Last Modified: Tue, 09 Dec 2025 01:40:43 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json
