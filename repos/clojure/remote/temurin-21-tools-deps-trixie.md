## `clojure:temurin-21-tools-deps-trixie`

```console
$ docker pull clojure@sha256:7adf2ca6380cdb5a894d94d0323fddbd78690864f7c7f5071a3347604d7c7bea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:fda4b77a9745c65bd1d2fde9c5ec87ddc3f0d09b92fa07be573b1a97e0fd3787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292718711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432ae8db81780cc045dc34b56707742d70d2d63dc1df27589c08ed7e0dd24f6f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:36:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:36:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:36:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:36:00 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:36:00 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:36:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:36:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:36:17 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:36:17 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:36:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682323fa16c395ae9c64b29615b78433655cf3babfef29df473b231c87e0555f`  
		Last Modified: Mon, 09 Mar 2026 20:36:39 GMT  
		Size: 157.9 MB (157857059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b904e955c7f946336be8278fba55231648e1b9aca6f00ad1fb98882f1efc79e`  
		Last Modified: Mon, 09 Mar 2026 20:36:38 GMT  
		Size: 85.6 MB (85567484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656d244d715fc3a41dc5fb168ec90c4bdaaadbc7a64bb56e1eb533acd81c684c`  
		Last Modified: Mon, 09 Mar 2026 20:36:35 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a13d7b9dcff265d590b560b2a6ed61805c52accde0cc490a425d86bc3c18454`  
		Last Modified: Mon, 09 Mar 2026 20:36:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:49019afaa3f055081eec73b711581eaf6bd765ae78fa110c83f1ecccab005506
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7488199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b898ac7e393c74ce2c2836b6834ef76106c25aa34ba8d067ae9c0772263fdd3c`

```dockerfile
```

-	Layers:
	-	`sha256:8594204df7025247d1678c2605fb2c8a516b3bf7409d283aaba61f73c4f481d3`  
		Last Modified: Mon, 09 Mar 2026 20:36:35 GMT  
		Size: 7.5 MB (7472445 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22440b763107781533a8a2fb414569e46354e13780610337c41c0ef2d6e19a50`  
		Last Modified: Mon, 09 Mar 2026 20:36:35 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bd871cbf6dc9a5823fc714a512ec4953444c7074138fa9d9360d6685376c06f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.2 MB (291169114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0ead1c5e634fe386099247fd025de5fa4d6403d210eae69468c9356c53fe83`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:35:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:35:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:35:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:35:57 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:35:57 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:36:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:36:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:36:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:36:16 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:36:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8334a5d5cfda220ab018796f5026779259df72b7b4244dd7a4e3d923c477f2a4`  
		Last Modified: Mon, 09 Mar 2026 20:36:39 GMT  
		Size: 156.1 MB (156133016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf631e68739250b35224b22d775e2e7b43860ad6f4bd005bd1c33deb165a5fa`  
		Last Modified: Mon, 09 Mar 2026 20:36:39 GMT  
		Size: 85.4 MB (85382888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f084b1ff39eadb63fa8a489c4c070e4a15b1c1f4bc0e4d6508f2946c9d5cdc`  
		Last Modified: Mon, 09 Mar 2026 20:36:36 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5c8f116a1e75e62ffd2486b17fc60014cf43066c896c8cc0ae87e060fcb4a7`  
		Last Modified: Mon, 09 Mar 2026 20:36:36 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2a814bd38815e515ca659e5d2a241280bfc3e358007eb08827b859c5cc32d4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7495347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52661f3dda7223c1e949850e49c2bdb254486805a31ed3b816f5f0d2ea73013`

```dockerfile
```

-	Layers:
	-	`sha256:1f9f41bdbdc21bc18b02f7b0705257836079574d3bca27a98bae2c39d6116d2c`  
		Last Modified: Mon, 09 Mar 2026 20:36:36 GMT  
		Size: 7.5 MB (7479475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c809ad418f203ca3d5463837f7a2a87b307f15c8470e5b3e2c0b9a94818eef9b`  
		Last Modified: Mon, 09 Mar 2026 20:36:36 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:00dbea6cae588d439b384813701fb794c55099ba48cbe2017b638cd86648197c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.1 MB (302067502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1688211606ccf65cdc151aeb86a78c25b583747bd3304fa90e8b56441e692243`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 21:03:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 21:03:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 21:03:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 21:03:29 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 21:03:37 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 21:04:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 21:04:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 21:04:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 21:04:58 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 21:04:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cecbee4d241c3e51c5833536e2a14e47748e3bf7f3563306f4afbb22a0345981`  
		Last Modified: Mon, 09 Mar 2026 21:05:58 GMT  
		Size: 158.0 MB (157977504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09986865d66dfeba3d3d1695420da6e5e9872d43ce93ee67de46b6ebe9eaeefd`  
		Last Modified: Mon, 09 Mar 2026 21:05:56 GMT  
		Size: 91.0 MB (90976694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993ece8f9a9cd48b3c9721bd6417438b9bd874f99e54d76fd14f7c1fac0660c2`  
		Last Modified: Mon, 09 Mar 2026 21:05:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805996622cedd24a9cb8c2df1a9d188766eebdae407a399ccad7edbab330abd1`  
		Last Modified: Mon, 09 Mar 2026 21:05:53 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:26799df9d51baa5d5894731a5bd67cf67ae471f76d225f079bc040f668a3408b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a60d2ba0c4f2e7a56dbb7cc141401082ea94ecb0e2a3837550e87918aac547`

```dockerfile
```

-	Layers:
	-	`sha256:04dca80598934e9eb060f6dbc5571a15ec977a22de17bf3c1b008bda3fd58118`  
		Last Modified: Mon, 09 Mar 2026 21:05:53 GMT  
		Size: 7.5 MB (7476866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0649854a198b65f383f41da4137c4b2a8648b3f5934ae1bcc3943a814a764eb5`  
		Last Modified: Mon, 09 Mar 2026 21:05:52 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:50c8a9932b9718040bea8102809803f06c4bec30220ac6069fa7fff9cac25957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289447453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee0fc21c023530d8fa1bc5e16fa83963164d4a0450870bd6052320042fc2fec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 04 Mar 2026 11:14:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 04 Mar 2026 11:14:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 04 Mar 2026 11:14:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 11:14:59 GMT
ENV CLOJURE_VERSION=1.12.4.1612
# Wed, 04 Mar 2026 11:14:59 GMT
WORKDIR /tmp
# Thu, 05 Mar 2026 06:37:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "21d16fbce3e546c4f0163c78aba0eb0293993c7fa1aba77d089fdbfa445e38a2 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Mar 2026 06:37:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Mar 2026 06:37:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Mar 2026 06:37:29 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Mar 2026 06:37:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3be247472b67578a1d05739722d8adeca41098796e5d6210800176db58046fa7`  
		Last Modified: Tue, 24 Feb 2026 18:57:42 GMT  
		Size: 47.8 MB (47776936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb9c79161005e6b84d0763b0f118c07cedf15f1b6ee06d958a2a83ad03907d3`  
		Last Modified: Wed, 04 Mar 2026 11:23:14 GMT  
		Size: 157.2 MB (157216889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e51cb875cac4a73a1c6a1988fbaa7e19fa11c0d81034af2ee1a9e11ac89419a`  
		Last Modified: Thu, 05 Mar 2026 06:41:58 GMT  
		Size: 84.5 MB (84452591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41747dead2efeda5162693591b552b02fdb3f98e26e074856b2e278195a55cef`  
		Last Modified: Thu, 05 Mar 2026 06:41:45 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e61b08696fb92c6a8afb10bf9520376f6b9b6abf8b98dec160735d8f11f496`  
		Last Modified: Thu, 05 Mar 2026 06:41:45 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cd50923c59cc03e02a1c2a7bb02e75fd23aef97150996463dc35c42549f11623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7476162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ae380548a37ea82341c1b5be8c8d08f5b5f561198692f5fa5764c123ab2e0c`

```dockerfile
```

-	Layers:
	-	`sha256:f67fd97995e9be3c0ec4c5e89f1b977394d0ac1e51f8b55a056eea17da6959ce`  
		Last Modified: Thu, 05 Mar 2026 06:41:46 GMT  
		Size: 7.5 MB (7460360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f5a9d7e309025850bd908032e51cea600368b952e25973c7329e07595665262`  
		Last Modified: Thu, 05 Mar 2026 06:41:44 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:05e7feee49e1351af917c5853b0bf5b7e434fbbc60a8ce27b71ac55153098e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282990871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00f32d8c2da90c04c138a0aa48d7329b02f1913120eb1e46c8857b5a1c7479a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:36:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:36:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:36:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:36:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:36:40 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:36:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:36:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:36:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Mar 2026 20:36:56 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Mar 2026 20:36:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae2feabd38c87cf12aaa6777865c8036e7e2b1e07050ea84bba18ec2494a27a`  
		Last Modified: Mon, 09 Mar 2026 20:37:29 GMT  
		Size: 147.1 MB (147105304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2586f2335338b1fac7c34f1f1130c4d09957b19d8abc9b22f951c3dc4deb0308`  
		Last Modified: Mon, 09 Mar 2026 20:37:28 GMT  
		Size: 86.5 MB (86529992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851d4c657d1fc0d7c44a5d2931ad23583d0338531dfabc1f94fc1d4a415bf242`  
		Last Modified: Mon, 09 Mar 2026 20:37:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3f799919f30831eef4bf6274590fc38bee3587dc3ce236479e3235446fa9c0`  
		Last Modified: Mon, 09 Mar 2026 20:37:25 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:db4a9968ffd190ef6d1795b9c627f6f5337f9eb68e008c2fe8015eb4e5cd4078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7484121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a897944775c588a3503f164f0df358781201b1aebbbf129ae739f427e33f1f`

```dockerfile
```

-	Layers:
	-	`sha256:3a7b67e2f03fa21397af57f7d270bf1d980dce746d4d91261f9d54ad01689ef4`  
		Last Modified: Mon, 09 Mar 2026 20:37:26 GMT  
		Size: 7.5 MB (7468367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7eac3ecd2e786c087343a0289c3f58d63d0805f70a45532b0d24537e31b128eb`  
		Last Modified: Mon, 09 Mar 2026 20:37:25 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
