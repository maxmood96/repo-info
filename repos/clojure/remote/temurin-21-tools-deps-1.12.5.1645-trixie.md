## `clojure:temurin-21-tools-deps-1.12.5.1645-trixie`

```console
$ docker pull clojure@sha256:3be3b6fa5a9116389b1459fbd080297382d2da3e08a365bb46351d116bfb1d64
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

### `clojure:temurin-21-tools-deps-1.12.5.1645-trixie` - linux; amd64

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

### `clojure:temurin-21-tools-deps-1.12.5.1645-trixie` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-1.12.5.1645-trixie` - linux; arm64 variant v8

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

### `clojure:temurin-21-tools-deps-1.12.5.1645-trixie` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-1.12.5.1645-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:3708f9dcca8477b129b4d5878dbc2ff83e645a9b0f95c7b37df3c7b1d063516c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.5 MB (302475333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e3998e523f8cdd08d0c3b8e27e28ab577735d96b17724a5cbd9d48d4502fe8e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:37:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:37:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:37:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:37:56 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:37:56 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:29:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:29:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:29:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:29:50 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:29:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9429fc219825eaf2a233c26bd84cdc3eef77eb70dd8fad888800a28c7609e2e4`  
		Last Modified: Sat, 09 May 2026 02:39:07 GMT  
		Size: 158.3 MB (158343282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c92b5ad6742605627d2efa917595a8445b128353d4e9c3a0de8107f1355286a`  
		Last Modified: Fri, 15 May 2026 20:30:31 GMT  
		Size: 91.0 MB (91007844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11fa0ae59bea57a9a771d61a1b4913ff9b02161ee79887648eeb33d3cdc4dcd3`  
		Last Modified: Fri, 15 May 2026 20:30:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935beca0eba42314e64327717881c1adb06ed766c8c7bcb82d5d87b1c7bf3c57`  
		Last Modified: Fri, 15 May 2026 20:30:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1645-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b55146ad7b53e9d4f442a29676cea844ba832f97740f12c6c35c340558f98ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162b1a558cd43ce0c519da9672c4c0776f6c71b587c3e343a0ce5cacfe172f71`

```dockerfile
```

-	Layers:
	-	`sha256:b7061d1d4792def69b8128fc678b36d1d4bd1a2f85d7eceacb3dabfe7cc4ce92`  
		Last Modified: Fri, 15 May 2026 20:30:29 GMT  
		Size: 7.5 MB (7477655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2d147473ea16c8a3f1949cc3d924156d8873ae0a5f05299de9d32b4888eb22a`  
		Last Modified: Fri, 15 May 2026 20:30:29 GMT  
		Size: 15.0 KB (15000 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.5.1645-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:1ab5b8087e0c10db45ceaa6c362a1ec9adf5b4db59e2aca8b30362a4033dcf1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.3 MB (283327779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c632483e81e9c231e5383aaa50e8ac4092767944cc732684b1246262ecd9a527`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 15 May 2026 20:29:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 15 May 2026 20:29:08 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 15 May 2026 20:29:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 May 2026 20:29:08 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Fri, 15 May 2026 20:29:09 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:32:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:32:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:32:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:32:07 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:32:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba69f29607ee8398fcf2e41d643b51acd78862008b319c7e3e63e96b8c2eb047`  
		Last Modified: Fri, 15 May 2026 20:33:06 GMT  
		Size: 147.4 MB (147388346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6687d2b60d636b6a69e62afa9a39bda0746c0f808a98dc9451c8b0e4ae9ca18`  
		Last Modified: Fri, 15 May 2026 20:33:05 GMT  
		Size: 86.6 MB (86566082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:289a8c68c7ae2d2eb10de5c937d4788461eb4aa08962a915442182c237fab2ed`  
		Last Modified: Fri, 15 May 2026 20:33:00 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58ea1c97b499c19bc089e9fc82bc7889cf2742ae478cf22f0d3cbf4ae72fdce`  
		Last Modified: Fri, 15 May 2026 20:33:00 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.5.1645-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:120c9be933e65fe310e873cc8f623e24cbbf6fc73a8f81ef2f49f61bd9d52539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7485064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6062010ad7ee99ecc9212720aec4e0d7dc4803dc99a6aa2e1660105212379b2`

```dockerfile
```

-	Layers:
	-	`sha256:2b4ceed1e961a94d425bf6eeac4802b33a50d0d50506fd896e8f57a000a556d7`  
		Last Modified: Fri, 15 May 2026 20:33:01 GMT  
		Size: 7.5 MB (7469156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0502c3bed7a9cba5fbbecd49d681a0090d2c3264425eeb035074bb00b9c2a892`  
		Last Modified: Fri, 15 May 2026 20:33:00 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json
