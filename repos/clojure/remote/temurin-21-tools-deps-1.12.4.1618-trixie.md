## `clojure:temurin-21-tools-deps-1.12.4.1618-trixie`

```console
$ docker pull clojure@sha256:e2d72be443857df62b1fed4d47b0067bcdf793bc7c104baa6b37c710955a318a
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

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - linux; amd64

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

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - linux; arm64 variant v8

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

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - linux; ppc64le

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

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:b2bee7d1b945bd20090753b55d3200431df96f9c614b6be607205e00c4878c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289447514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bfac613d180309f0bd327508635ff00cf128064f8b30d3ab36b36aa88ee42dc`
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
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 04 Mar 2026 11:14:59 GMT
WORKDIR /tmp
# Tue, 10 Mar 2026 01:38:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 10 Mar 2026 01:38:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 10 Mar 2026 01:38:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 10 Mar 2026 01:38:21 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 10 Mar 2026 01:38:21 GMT
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
	-	`sha256:b5d5d02f7b83844a0868dd8f028cb57a1e57e909bef42be92d11b6b50e8b301d`  
		Last Modified: Tue, 10 Mar 2026 01:43:41 GMT  
		Size: 84.5 MB (84452643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f29f76ac2f6c85f320d15da81852d9b4131e3fb9a62e14d0c95e9f4d9e16a1`  
		Last Modified: Tue, 10 Mar 2026 01:43:27 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d656f73699437c686c7a8edda71370a40c3be091dc8b87ec77acd4c2319ffc`  
		Last Modified: Tue, 10 Mar 2026 01:43:27 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6fb342b904061038b1b61d44537c3e2e39c0338c8a08809c5eff2a3b48c26746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7476160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b03329ddf893905ed1fef04f18932e04dd75b3098945e999cd352187ff79adfe`

```dockerfile
```

-	Layers:
	-	`sha256:fc6d338096b4c6dbf524de47838de6061d4aa15e54e11e3b58fc32919a5e20c6`  
		Last Modified: Tue, 10 Mar 2026 01:43:30 GMT  
		Size: 7.5 MB (7460360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:936695ff712e2e37b93456b0d5ed96435c0c60768ba8ae6c350f8c343eb4e556`  
		Last Modified: Tue, 10 Mar 2026 01:43:27 GMT  
		Size: 15.8 KB (15800 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - linux; s390x

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

### `clojure:temurin-21-tools-deps-1.12.4.1618-trixie` - unknown; unknown

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
