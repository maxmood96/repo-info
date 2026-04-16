## `clojure:temurin-17-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:456cca7b30fe8e8439481315bfbac05cffae8f33e64ec9ce794572c667b4126b
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

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4adb5e65a31420fffe0ae51b37e5494005db07d5ec477f0068745250675412b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243565158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02d8142669fad3cc0985a617d471c267b581453fde4de9054d2c757651d26be8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:04:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:04:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:04:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:04:14 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:04:14 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:04:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:04:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:04:28 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:04:28 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:04:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:da539b6761059a0a114c6671f1267b57445e3a54da023db5c28be019e40f0284`  
		Last Modified: Tue, 07 Apr 2026 00:11:03 GMT  
		Size: 28.2 MB (28236332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0445e9209bc7fffc61cc34dd35b140bfd31fce266977e15cea579a50c6678938`  
		Last Modified: Wed, 15 Apr 2026 22:04:50 GMT  
		Size: 145.6 MB (145628750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6305fa441cda656d27508c455dcb2f85d26d44310d409ddb11f44405ad358116`  
		Last Modified: Wed, 15 Apr 2026 22:04:48 GMT  
		Size: 69.7 MB (69699034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8796477b9b1b7179f822c3c97d01da2f6919c0c38f1336341d4ba8ec37c6faef`  
		Last Modified: Wed, 15 Apr 2026 22:04:45 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37096caea4f666c5a390009519be8bba220f265aa2a43df398b4e8b94ad2aad5`  
		Last Modified: Wed, 15 Apr 2026 22:04:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a5f006678e20b25434f1a3da87f3237a07354bf011792b2a990ca4c09acdba63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5132001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643517ddcfda85125ad6ea72fac164cb7d78d4273eb4c9bf3d35a0d229273f9b`

```dockerfile
```

-	Layers:
	-	`sha256:ab5dd1cc40db9ecc31eda938d85cac3449267edca6847a8a056038b7c3bcf8e6`  
		Last Modified: Wed, 15 Apr 2026 22:04:45 GMT  
		Size: 5.1 MB (5116167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7094ef20895391cb4c4b6d1a455133e9f49d0890fd33a3cc7e1684a991c9909`  
		Last Modified: Wed, 15 Apr 2026 22:04:45 GMT  
		Size: 15.8 KB (15834 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:07285d534910d4c30230f74ac8559029d7bb0de0a60158a330a1f9baa70202ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.2 MB (242244514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ceaddf8c4fb9ca47f1435f7254a0af1ce6bba5b698390b635418814df0cb4a3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1775433600'
# Wed, 15 Apr 2026 22:15:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:15:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:15:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:15:32 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:15:32 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:15:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:15:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:15:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:15:48 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:15:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1dbbb2db815c2527e90ef5a3e4dfb957cfe7b61b6a7fc59722f1f64b1a1b611e`  
		Last Modified: Tue, 07 Apr 2026 00:10:39 GMT  
		Size: 28.1 MB (28116166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe2eb0c07bca127a9a6f6c686331481ae65a65fd10aa1f5706be81f4c697512`  
		Last Modified: Wed, 15 Apr 2026 22:16:12 GMT  
		Size: 144.4 MB (144436254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5747a5caf67e27a045f61fc5542ac83792ebd9157f7bdc28960dbd6b4c6d795`  
		Last Modified: Wed, 15 Apr 2026 22:16:10 GMT  
		Size: 69.7 MB (69691049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1256204316d80ee6c01c7c9be1491a3d6b7bc8b08b396bf8ecf6ac5c550cfa`  
		Last Modified: Wed, 15 Apr 2026 22:16:07 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7511a23fa6ef3e6dfc7d041701d822f3257695663176a405c378f93d048b4186`  
		Last Modified: Wed, 15 Apr 2026 22:16:07 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:20e8a3dd3eaf85f9018fe722d22356a591359409ea6219a44a2f8dd1d585f481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7895f0a52f6d5c096da0ceea1cec6ff2cbaeb94f730a9f7572c3d9944d66936b`

```dockerfile
```

-	Layers:
	-	`sha256:28092115f3dc4d4253dcfb2d4d980dd600297a3ef6f087a04dea45016661439a`  
		Last Modified: Wed, 15 Apr 2026 22:16:07 GMT  
		Size: 5.1 MB (5121928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b1d2c11f4abb6bdbebe8b79c353bc98331ac27be4f899d75917ff8be3b60d00`  
		Last Modified: Wed, 15 Apr 2026 22:16:07 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:127b00f44d4ca95894a6270dd12294176e849df470840527a7274100eb77f359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.0 MB (253047297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf2a4af3db8d7a12afd1a679fcc8a2ed83f5b5fba948fa399f9f96cfe601e1fc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 02:49:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:49:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:49:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:49:09 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 02:49:09 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:54:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 02:54:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 02:54:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 02:54:25 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 02:54:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b1c56220ca211bc9d02f1ed5c589465809676b6ab2cef705f1e2fb8e9726de76`  
		Last Modified: Tue, 07 Apr 2026 00:09:42 GMT  
		Size: 32.1 MB (32078464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac07d766af011abbea5aa154cb16be5509f5ea8687e2050966b40181dcca495d`  
		Last Modified: Thu, 16 Apr 2026 02:50:31 GMT  
		Size: 145.4 MB (145438295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be861dbe36138889a98f1a69d8a1492c0ec1cdd48894d0f2a74d018b769865ae`  
		Last Modified: Thu, 16 Apr 2026 02:55:05 GMT  
		Size: 75.5 MB (75529493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4745bed3e6e3c11c73aafa9a6fc3620938cd2a60bd8c27a5beb2deb3863fb61`  
		Last Modified: Thu, 16 Apr 2026 02:55:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce9273f10bc056901c484965125ab10fd2a2db64ce330d93c2326343dc2e647`  
		Last Modified: Thu, 16 Apr 2026 02:55:02 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7634b146b0237e2032c1334ef8521eea240824fd2fd9b17ac65df9766e741233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5137208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845664851705c6e7ae1d1a480b1da8a421d99f3438944b389a1df1914b898e52`

```dockerfile
```

-	Layers:
	-	`sha256:d3bbcc9b9f3882410814704ef3a8c561baf0cba6a24bccae0eb3613834077ed7`  
		Last Modified: Thu, 16 Apr 2026 02:55:03 GMT  
		Size: 5.1 MB (5121325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:077fde46c4e473e146c4130146dbb913dd04c3d0d3d38cd1c7cbd1c3063ebf14`  
		Last Modified: Thu, 16 Apr 2026 02:55:02 GMT  
		Size: 15.9 KB (15883 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:651cd07ba88ee63b1e23fc22eb5c46261c38d2ee8873bf5234ba757d02db9f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231032473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e25fe6b6ba3991e908c36c59dcc5f87adde47919c37b166f4111404ec63f25`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1775433600'
# Thu, 16 Apr 2026 00:39:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:39:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:39:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:39:13 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 00:39:13 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:39:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 00:39:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 00:39:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:39:27 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:39:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c23087fbbda0d8352ee6b2d159c503459acb89da0eba1729b411ca394e68e292`  
		Last Modified: Tue, 07 Apr 2026 00:10:59 GMT  
		Size: 26.9 MB (26891634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fd6332338077f5cfab2da5c3f9c41f87afef5299826bf5dfd0ac5efa3170bc`  
		Last Modified: Thu, 16 Apr 2026 00:39:55 GMT  
		Size: 135.6 MB (135627002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42fd8d08052ed67012143fe7b97ae34e3dffe077ceacf707eeb89d21b5414dac`  
		Last Modified: Thu, 16 Apr 2026 00:39:54 GMT  
		Size: 68.5 MB (68512794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c56dd55b16bda4d9076036fbe5cad1641b7a12715454d0976e95751987362571`  
		Last Modified: Thu, 16 Apr 2026 00:39:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a45347e0e1add0d14ef43e2dc69c2552d01800d2f390dde977c26880d8d9a48`  
		Last Modified: Thu, 16 Apr 2026 00:39:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1f7ea147a195dc4a8c430d007d0a4d5e9850459e83fdbb1064406dfeaf5f23db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5123324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad81e5ab88a02db66e1bc004b2123c8a99417bc8882bbf2465b23a4e47f2ad36`

```dockerfile
```

-	Layers:
	-	`sha256:174168bf4d6c93c856d142e46a14fe9a4ca0ae86287acf2666acce25165ffcf2`  
		Last Modified: Thu, 16 Apr 2026 00:39:52 GMT  
		Size: 5.1 MB (5107488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f13459a5ed5ecaa7fec06d510c5ce2ec906ff709bc76340281a03a636e134ff`  
		Last Modified: Thu, 16 Apr 2026 00:39:52 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json
