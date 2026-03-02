## `clojure:temurin-11-tools-deps-trixie`

```console
$ docker pull clojure@sha256:90eda7696f1c84624546b169de7a5e3bb4e97f99e9da44a01fe2729f76cdf22c
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

### `clojure:temurin-11-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:65af8dcf863fe4856ab5a16bb5801b883efbf4e5629b4a4a91fbc4166a9f8738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280655214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9812cd63a3e9c75351b8f6a6a456272012f58115b5e999e9f425c9bc7ddfd91`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:46:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:46:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:46:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:46:10 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:46:11 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:46:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:46:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:46:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f902517047a28941e36c8bfea2cc4261b97a3f64e7398771906b55c6ca96d95`  
		Last Modified: Mon, 02 Mar 2026 19:46:53 GMT  
		Size: 145.8 MB (145806770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9347e0da99c6708ff9ff6213e8b50cf18961e9b39b3993706c0f51a9f9272413`  
		Last Modified: Mon, 02 Mar 2026 19:46:50 GMT  
		Size: 85.6 MB (85554672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab15c136feea81b1a26e5fa959bc12cc5590fba8a9de3ece273d519bcba3c7e0`  
		Last Modified: Mon, 02 Mar 2026 19:46:45 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:592417cbf1e9e4b0e8403a6543f2a881564300063f98f5ba471b1fea5798e75e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7504919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f07de6a2bb4f2136268875757881d1c7f47d87292000b0c2cf1895ffa5732d5`

```dockerfile
```

-	Layers:
	-	`sha256:c034bfc136b6ad638e8aa3fe3dc099f5aa86c0e6f28b9a5c701fb9b062611c5a`  
		Last Modified: Mon, 02 Mar 2026 19:46:46 GMT  
		Size: 7.5 MB (7490734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:478a08de422f48bbb25f26527a2620fb24894013d19ba107fcc70452a26cf031`  
		Last Modified: Mon, 02 Mar 2026 19:46:45 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:58ec7a294fca415994038b01781f90c3798bc315e553cd86209df2dd4153cac4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277532634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cb37a1472c4c5448bb9299b7a8822223e9ec7365442a5ddd15bd2405f726dea`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:46:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:46:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:46:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:46:08 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:46:08 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:46:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:46:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:46:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae09b3923b9fe0f28f97c656ef294508cac00cd44ce716b1273ab9f5265c1914`  
		Last Modified: Mon, 02 Mar 2026 19:46:52 GMT  
		Size: 142.5 MB (142501446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d563b8c4fbd6c7951556421af89d178feee02bc19ef61f62c88fe953d39aba5e`  
		Last Modified: Mon, 02 Mar 2026 19:46:50 GMT  
		Size: 85.4 MB (85378374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d4030919f57a1a9e63f48f6a990c1cb24fd6c2fbcb2497f1cde6192f560b71`  
		Last Modified: Mon, 02 Mar 2026 19:46:44 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3b74431023fbfc41fe9ccc7f5e0fa3711a870e254e07ed844bcad1efb3aa736d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7512685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93db4b0fb8d6c0efd606659bb409c109a2cac62901d03c60bd22cc1fba452afd`

```dockerfile
```

-	Layers:
	-	`sha256:3eb8ffb24b9af656c879594865dbd8e3a1c6c7ae05e87ec5ea58d4dafe57fd97`  
		Last Modified: Mon, 02 Mar 2026 19:46:45 GMT  
		Size: 7.5 MB (7498382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc2e3c3b46c619373712b4302285066f87da06129745652c512995924da308ce`  
		Last Modified: Mon, 02 Mar 2026 19:46:44 GMT  
		Size: 14.3 KB (14303 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:50f5561410cb90e4dd6747df69244d75128cf592139f4d279698870b3261cd89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.1 MB (277084823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1914481699652191dc9152a4a710a7712403bb2417aa6a01826442cae490c211`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:53:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:53:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:53:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:53:29 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:53:29 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:54:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:54:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:54:30 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d9b137c5054ec827ac8f17b88ceb1aa674586507b1aa80d67b3de14aff2ab2`  
		Last Modified: Mon, 02 Mar 2026 19:55:19 GMT  
		Size: 133.0 MB (132997811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3452980e901cf0e3cdf2add10232f0c5ef1ff0bc9fc2916b0a2c86e635a4a5f1`  
		Last Modified: Mon, 02 Mar 2026 19:55:17 GMT  
		Size: 91.0 MB (90974103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad51786762177f01ac14193e6e6400b33605ca6f85eedfb3f87dd4a7034b0c5b`  
		Last Modified: Mon, 02 Mar 2026 19:55:11 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b0c3b0f936ffaa12b541d369f93da29b0a73e0b5947d79b24b62b53d13b5173e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7508772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fb45371a76c845441c5cbd2dc76016faa0bd66da8eaefa76d0edd5b0c8da61a`

```dockerfile
```

-	Layers:
	-	`sha256:d99b5daed953a451103009888b2d80e4aedaebb0299548c43ce295623132f0b2`  
		Last Modified: Mon, 02 Mar 2026 19:55:11 GMT  
		Size: 7.5 MB (7494540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08ebc2b5d68289bb524be8832fdd86951c4c60a5b565fd80274684441f90ed24`  
		Last Modified: Mon, 02 Mar 2026 19:55:11 GMT  
		Size: 14.2 KB (14232 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:265d90a28cadb39bb7f07cc9ec3ca0189bc0a30ac1c83d84db0390345d3b2a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262448067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffc6f0b2dcb083c2da5f50b92f9e06271c6ec14cb5696e479493d1c4bb9c9fe`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Mon, 02 Mar 2026 19:44:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:44:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:44:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:44:59 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:44:59 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:45:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:45:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:45:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4096ad5f60bd954b10f9424d415e32f836ecf2894fa34b13f1cdaeed415f14f`  
		Last Modified: Mon, 02 Mar 2026 19:45:51 GMT  
		Size: 126.6 MB (126562061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265753c9ab04125b282a03008d019d32bdcfb8e56605fe96d95e34dce6e2e434`  
		Last Modified: Mon, 02 Mar 2026 19:45:50 GMT  
		Size: 86.5 MB (86530825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1cf9618e4e9f037e857b63b4ed0f1d890396a7f8d1a73d0c5acfa5d71cdb4f6`  
		Last Modified: Mon, 02 Mar 2026 19:45:47 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:98b751e3ae69fdd6fa469dc59f36adb6d184140c635b4097f2ef6c56f3d95346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7500845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a6f7661b812a0b53123f26a1cb30ae7ac6cea869a01d0cc684aebf1578e3ca2`

```dockerfile
```

-	Layers:
	-	`sha256:7ef8851eb95bd1aaf97564c11fd0262cde7d06a1ddebf8a35d7ca2ae97c7b57a`  
		Last Modified: Mon, 02 Mar 2026 19:45:48 GMT  
		Size: 7.5 MB (7486660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f3729eea3ec1bd8da0e52e264431cd19e5e73b8ab5593854fc3d11b552871c1`  
		Last Modified: Mon, 02 Mar 2026 19:45:47 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json
