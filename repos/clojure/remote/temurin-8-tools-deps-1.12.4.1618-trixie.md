## `clojure:temurin-8-tools-deps-1.12.4.1618-trixie`

```console
$ docker pull clojure@sha256:86f3fef4fa95f2ccb149206dd7973071a7ca187c18b410630df8941f86889a4f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.4.1618-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:cb4d1f0163dd0627efaf4b1397473f6288173d9bd04f750ff58bd78e8d6d4a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193550432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d8eb91cc6afab59a5223407fece8aaee42c3fcdd37f05f5ca1bd8715a76cc7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:01:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:01:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:01:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:01:51 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:01:51 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:02:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:02:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:02:09 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a7730063fcfe708b222d34c4f07d633dfe087a28c05c4daaab2fa9943854c155`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 49.3 MB (49297833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b099a692a58bfd49ed8958f65483bd10fead8c0f50ba4bf3b09ad4cfc70c64b1`  
		Last Modified: Wed, 15 Apr 2026 22:02:30 GMT  
		Size: 55.2 MB (55170118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97028e3116a8423597267859563c194a2ec4e717daa1f13d8dac27effda7c30f`  
		Last Modified: Wed, 15 Apr 2026 22:02:31 GMT  
		Size: 89.1 MB (89081835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51f69a4caa30723b9e8d358fba73332d18ef0f3a2a73f87a6c06696bd363ff5`  
		Last Modified: Wed, 15 Apr 2026 22:02:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e65a7cfd4ad6b314b8ab3b29f5cd5c1d0e1a6f926109de7d73dccb1389b3fa61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7605824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7d817a06ef8139e1b622c391d02e9d22425b79f162a1bdb414babaa2954860`

```dockerfile
```

-	Layers:
	-	`sha256:0a2850d47428446daab0b84e7119fad5a6d58ad25ab8e3374b69f2f530088d36`  
		Last Modified: Wed, 15 Apr 2026 22:02:28 GMT  
		Size: 7.6 MB (7591654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c663dfda8fe30789c38d217ccb4b902b73003d8459313d01ce2ef5200252bff6`  
		Last Modified: Wed, 15 Apr 2026 22:02:28 GMT  
		Size: 14.2 KB (14170 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1618-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5bcbc6636dbc9c161aab6536ba8a2043c44ce9a839c30af870523c106a20acb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 MB (193171093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643f7ead4dc7e9e35ac5acc4cf40a1b443fd7a13d26cf751cd5b547530989955`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:13:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:13:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:13:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:13:11 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:13:11 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:13:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:13:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:13:30 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:912041a7b9f63b6550d3a3949c43e45f74a36a2f80c727e70e41cbe851de2d20`  
		Last Modified: Tue, 07 Apr 2026 00:11:19 GMT  
		Size: 49.7 MB (49665256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaf693ce8c236550ab90c4e8ee3d7beb1d36d69f546df4761abe09f7a5c3850`  
		Last Modified: Wed, 15 Apr 2026 22:13:51 GMT  
		Size: 54.3 MB (54251614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd0b5165af493d77a264290f94ee27b7aeeabc6097023f3a38c3f9b6dd4c69a`  
		Last Modified: Wed, 15 Apr 2026 22:13:52 GMT  
		Size: 89.3 MB (89253578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98178115b498b56df388081aab61add9ad134ea28ebd2ecffbc8a99be512b45c`  
		Last Modified: Wed, 15 Apr 2026 22:13:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ef97844ea153dd182a0e541da7f61b8ae4704bfc45b25f6dac4ab90eda1310ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7613672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc87b5dfd918708b7b6b850cc56e97eb1bfb58eafc933dc4102ccd5eb72e96fc`

```dockerfile
```

-	Layers:
	-	`sha256:8e91262894b9d6b6a3287fa8c7b67c2d923f069c725b6e5bbf8711e0472987c0`  
		Last Modified: Wed, 15 Apr 2026 22:13:49 GMT  
		Size: 7.6 MB (7599384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba405ee012c3f240e0126833a66360cce4c3a08da661feab6d17f35b54b81642`  
		Last Modified: Wed, 15 Apr 2026 22:13:49 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.4.1618-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:9a28409b41383cfdef7e22ff8ad71b555fe2dce9e62bb8976c2f47f2b5979fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.5 MB (200491991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7df4fc872cfeb1f40d89f87b3040096d1705b9bed59c52c851e920078e498f18`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 02:32:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:32:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:32:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:32:58 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 02:32:59 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:38:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 02:38:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 02:38:18 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f2bea5beaa06af8495b6a91d35dc5ce3b11a84dad25d5c0a468a1e7008ed9e62`  
		Last Modified: Tue, 07 Apr 2026 00:12:52 GMT  
		Size: 53.1 MB (53118669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d12c2460cb3461975521962c8f8a97ebe891068bcf626491de7565aee72a3dd`  
		Last Modified: Thu, 16 Apr 2026 02:34:16 GMT  
		Size: 52.7 MB (52650393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c31f1a2b7c617893d6bbd436284ee2717f4af4c0343d245af5139da836ac3b`  
		Last Modified: Thu, 16 Apr 2026 02:39:00 GMT  
		Size: 94.7 MB (94722283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8e28f413ef49271157ca5929e8dbfe765a2532ee4e15aec39a7b1ed13933f5`  
		Last Modified: Thu, 16 Apr 2026 02:38:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:47a9f53366ff939c332c663e27654fd859fc52de700cc121f4caebaba172cc2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470508a9c1d53d406effb135fff688359d34e55f76f71634024413ac201de2db`

```dockerfile
```

-	Layers:
	-	`sha256:4ed710680943844ee82c4d4a2d94d5a0799a338d6109e1387966573ef848073a`  
		Last Modified: Thu, 16 Apr 2026 02:38:58 GMT  
		Size: 7.6 MB (7596670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4dfed83f77e17d3aecc32a54a94b9f943231f538caf3ee694a6728e21393ed3`  
		Last Modified: Thu, 16 Apr 2026 02:38:57 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json
