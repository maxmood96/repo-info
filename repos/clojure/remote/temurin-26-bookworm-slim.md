## `clojure:temurin-26-bookworm-slim`

```console
$ docker pull clojure@sha256:244eb7d1ca206fb7331a0fbf238faaae1e3097c5ae1de2c9061707e92a78a850
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

### `clojure:temurin-26-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:46efb52d6c358eb0fb2a293c74446f121dd139d4beb8e3f8a4de93e624ee2c4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.4 MB (192423818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d34a35dcb854a11d91ae2b7fff8a7cf56d60f30a1cfd83ed8a2cbe86a40a0f6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:36:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:36:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:36:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:36:50 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:36:50 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:37:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:37:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:37:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:37:03 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:37:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9b02e9fcb40102eae20d9d1fc7594b44328f4a3eb9b8a3bdb7db283d10840a30`  
		Last Modified: Fri, 08 May 2026 18:22:44 GMT  
		Size: 28.2 MB (28236282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf92a5955922ee22a6df69663540c53297cf9c0809662f2c60a9f8cfae9687f`  
		Last Modified: Thu, 14 May 2026 23:37:24 GMT  
		Size: 94.5 MB (94455681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30254eb68dadddea5a19afd79860ca0ec7d351ee2ff270a25d32769da1591a4`  
		Last Modified: Thu, 14 May 2026 23:37:24 GMT  
		Size: 69.7 MB (69730812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23782a01cc0fb9c50106ccdf638730690bc9244fe50f4c5030668f15bb9cf351`  
		Last Modified: Thu, 14 May 2026 23:37:21 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccacc768a871f0f080f30b008f3d93c1edc5e28b4d91b3cf18d596b699d4698a`  
		Last Modified: Thu, 14 May 2026 23:37:21 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bcea7edaaa58fdc6b67e42abc6aa819ffaa8e651dd367fb8858584f1679a1e63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920a52fa5d929ba9c539c279b3414833a7a3a39c5a2dfdb6651da816a5088f22`

```dockerfile
```

-	Layers:
	-	`sha256:f1d952ea10505ec1fb3668547567cde95cc3abbbbbc324cad7c840434e6297e2`  
		Last Modified: Thu, 14 May 2026 23:37:21 GMT  
		Size: 5.1 MB (5081669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43ff0354c7d06aed28cfcf85197fc476f5af255b86fe67c7f85d5afd22362989`  
		Last Modified: Thu, 14 May 2026 23:37:21 GMT  
		Size: 15.8 KB (15829 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d08a25557e19868e639caf7294594f01053f61d2db7709baa3f503ff0b030677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.2 MB (191234749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faceb2e70812e5e90718a495be67e545674f24799a31e120b2d6b36acb803714`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:36:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:36:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:36:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:36:59 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:36:59 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:37:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:37:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:37:13 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:37:13 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:37:13 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a2d07df495cc055bce0251fe801ee08db90750f52e43a555be5dfd8f5023783`  
		Last Modified: Fri, 08 May 2026 18:24:52 GMT  
		Size: 28.1 MB (28116165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a551ce66d778ef372e46d760bd51a18eeb227d08de14e2d71d77fcde349f60d7`  
		Last Modified: Thu, 14 May 2026 23:37:34 GMT  
		Size: 93.4 MB (93395168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2973355ba51f57bd6fa47af9da99711936ce71d0112c570b76deb2ef419359f4`  
		Last Modified: Thu, 14 May 2026 23:37:34 GMT  
		Size: 69.7 MB (69722372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eda57d87c7f001368d2e2802b2d004c099c45e2f9138881a35dec7191733817`  
		Last Modified: Thu, 14 May 2026 23:37:31 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5d51d1afd3f7707ee169366ebe5e7793d3f94d2e3694e378b38160efc73094`  
		Last Modified: Thu, 14 May 2026 23:37:31 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:12f9711399d0019fe238d86a7c85fbc86442c699def5e99d450c8d6d0ec3a47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5103374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c5055e564a8f73b4d130e2b7f5a8f7b4ea1fbd8b9e9e4117a237ba53623a821`

```dockerfile
```

-	Layers:
	-	`sha256:4741196192e87640a612e74080fe1316f685bb09cc895d1c9c28af78cc8cc1a8`  
		Last Modified: Thu, 14 May 2026 23:37:32 GMT  
		Size: 5.1 MB (5087427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7f3bc32807e8b49f42e04978f7bfc64393d1d20b4c57378af6da60519070faf`  
		Last Modified: Thu, 14 May 2026 23:37:31 GMT  
		Size: 15.9 KB (15947 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:7d73929effc2a4d0e54d491d90496a0d740944caf32d72c5c6a24e12c003cef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.4 MB (201426986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaac3d6d485c02a131821522a737af89a940e596fef4dfe947c07647d338d159`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Sat, 09 May 2026 02:47:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:47:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:47:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:47:26 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Sat, 09 May 2026 02:47:26 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:57:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:57:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:57:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:57:36 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:57:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0e29ea7436ed4beb1c38bcfee44589407e49fc690669b42b35db33a9588e820a`  
		Last Modified: Fri, 08 May 2026 19:44:06 GMT  
		Size: 32.1 MB (32078453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea74e2d5f082a4e3bed610cad5118f31172b96baa2083e47ff5cde42b672f30`  
		Last Modified: Sat, 09 May 2026 02:48:28 GMT  
		Size: 93.8 MB (93781494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0282dd6262cf34219e3ddeea4b475b484c5ae58ea9e326dc74a3cb02b95c89`  
		Last Modified: Thu, 14 May 2026 23:58:43 GMT  
		Size: 75.6 MB (75565998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61966a81f4e378f9e001620412beebe30e8739de98f95927663c19ca4d17177`  
		Last Modified: Thu, 14 May 2026 23:58:41 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d98cc6237c149a1ce52665759f6bf1ce1ca67f885528ad94cc1d51f9e444e85`  
		Last Modified: Thu, 14 May 2026 23:58:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:75826147fd5caa4c3a0fe515daec127fdf5730e89665b4abf54dc085a1dc568e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5086640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d73b2c6d8dd5041a731d9aac0b5f04fd39cf6ceb06a6442a68056d825eed89`

```dockerfile
```

-	Layers:
	-	`sha256:bfeebaaa418623845846307524ae3fb5fe017d56e78340008afac675687c3b48`  
		Last Modified: Thu, 14 May 2026 23:58:41 GMT  
		Size: 5.1 MB (5070763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a434bd29752d6e09432e08f762359889ca4fae8d8d521a73556a9dc4427e285e`  
		Last Modified: Thu, 14 May 2026 23:58:41 GMT  
		Size: 15.9 KB (15877 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:593d979736418169c683f5ba6f3cb9110b36495b3501a8ddcac550e3e1cfd36f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (185984525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787616f681c0d5f09a9c2ad77cd26d585d63a89bbbfb7f7f769f5703eb65bf49`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1777939200'
# Thu, 14 May 2026 23:38:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:38:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:38:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:38:59 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:38:59 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:39:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:39:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:39:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:39:12 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:39:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8e45267b009b7e1018e83fd0f228ba0ad9b97aea9f10520c2d76c3baa70dfe01`  
		Last Modified: Fri, 08 May 2026 18:27:33 GMT  
		Size: 26.9 MB (26891602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941d8a13d14a16f71a9f808e596b9057ef487aafb691feae3a438a6df5846bad`  
		Last Modified: Thu, 14 May 2026 23:39:39 GMT  
		Size: 90.5 MB (90547731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e91f907b0d23fbd27d79fa47299c4ed6d1a3f0a39966d4ca3b713b6824b929`  
		Last Modified: Thu, 14 May 2026 23:39:39 GMT  
		Size: 68.5 MB (68544150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153e9671d34c6c72a03013dc9a6319895b0629eff8c66dd69df8aa3d0dac43ed`  
		Last Modified: Thu, 14 May 2026 23:39:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30aa6590b678952762d291fc4a8196aafff76adad4fd4fd3935162ce2d858c51`  
		Last Modified: Thu, 14 May 2026 23:39:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bb1e9a8f53ec7d072c4669aac8af5baa3aabc677785142d649d93e5dad6af437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5074005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f17d86418e5c26c76a09b243ef06abff2633f0a3ed0f33f7ae17196c6344b31`

```dockerfile
```

-	Layers:
	-	`sha256:36545cc5da961010386c4b40b6796e470c28cb0f87d56013007c4b6d8dd57159`  
		Last Modified: Thu, 14 May 2026 23:39:37 GMT  
		Size: 5.1 MB (5058176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4e9bd10e3b1e63bf76aae9dcd9c2e8e146f70524e1e3830375ffa505979879f`  
		Last Modified: Thu, 14 May 2026 23:39:37 GMT  
		Size: 15.8 KB (15829 bytes)  
		MIME: application/vnd.in-toto+json
