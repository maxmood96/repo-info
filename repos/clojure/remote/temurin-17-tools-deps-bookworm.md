## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:fb1844854ce17bb99542099d029b25b4ee1e3f2f5bb74e46e700f535d94f4500
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:6b1204a7315ec469f4c6d7b013204e99447199866dd8f2d308d15c44f89da1c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275190473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9bde59a2dcb25cdce0d8ac621bee964493b05df471c970d11fc26f0c50d86b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:1129dcf71f67461f4730620f8148cc9ebc7641966fa683cdf84807219ad288b2 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8cd46d290033f265db57fd808ac81c444ec5a5b3f189c3d6d85043b647336913`  
		Last Modified: Wed, 04 Sep 2024 22:33:56 GMT  
		Size: 49.6 MB (49556702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1873ef51bdcca3e237da7aa54aae4c5b7d30f27914dabb6175706483a6700fd3`  
		Last Modified: Wed, 04 Sep 2024 23:08:02 GMT  
		Size: 145.2 MB (145166536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fb0e7f5fc52606fc523a36076991441776adb7b44254d1de81564422ca6e75`  
		Last Modified: Wed, 04 Sep 2024 23:08:00 GMT  
		Size: 80.5 MB (80466195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39178358280018db0a06aa31087ba633c6147d99337a95ff2590698b7679f26`  
		Last Modified: Wed, 04 Sep 2024 23:07:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43577a486484f9ba7efa2643dddea35f7cd4cd94941fbdb0f6fb62381160f8e2`  
		Last Modified: Wed, 04 Sep 2024 23:07:58 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fe98999baa85b840ae2c119bc75738277fbb342c29b1bcc714759793975686e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7014911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3653511bc407ac3162ecf77a351fa25a97096571a683bec7fef828029ff7b604`

```dockerfile
```

-	Layers:
	-	`sha256:02de887ba461d295e983edf0f542011fc6ee3acc0c767cab6bd25d732dd2043f`  
		Last Modified: Wed, 04 Sep 2024 23:08:03 GMT  
		Size: 7.0 MB (6999471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b05bf7eb735b29fa0cd86c821b74808b6e58974303b436e1f75b91f03ce8b22`  
		Last Modified: Wed, 04 Sep 2024 23:07:58 GMT  
		Size: 15.4 KB (15440 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:016774df15a57e26b1a0475d2c1c985d623c0450973a0a164aa4a1565688d372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.8 MB (273757225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54fe2cadd903e03845971a477d69d62ce20efa7749c76c6bb79c310409e25ab1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:7f28c8fde9feb67359cbf19f7d77d3f757490b5f586520257cf92d233b4bfaa4 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:56c9b9253ff98351db158cb6789848656b8d54f411c0037347bf2358efb18f39`  
		Last Modified: Wed, 04 Sep 2024 21:42:16 GMT  
		Size: 49.6 MB (49585623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1c47a4cd5930dd2c3781546d732cb55a805ff918fbfbc04015d255f7134ae0`  
		Last Modified: Thu, 05 Sep 2024 08:01:55 GMT  
		Size: 144.0 MB (143959444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4794e31236df99de650781dade0891ad76d2913eefbc281583f9d68c3e5893a6`  
		Last Modified: Thu, 05 Sep 2024 08:05:42 GMT  
		Size: 80.2 MB (80211117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6547169f50917f2fdfff34e106f16948ba0b8517c3c3b8b765e40c766813d134`  
		Last Modified: Thu, 05 Sep 2024 08:05:40 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b0aab5c85652327dcf69d88795c2fdbab1cbd60823d1aa02e9b39e97ecc4e6`  
		Last Modified: Thu, 05 Sep 2024 08:05:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f042f067c1f61db58053faa0a2db4c4181c6f5bef570a3ceeab124e2fee79fe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7021834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07213cc043955fa17d02966f8a17d3014c5e37bb5e71802e0754d27048d01923`

```dockerfile
```

-	Layers:
	-	`sha256:b800834ad3d55d28cd85f1c3f51885fe750ed8db6ceb5e1e664be53b578ce3e1`  
		Last Modified: Thu, 05 Sep 2024 08:05:41 GMT  
		Size: 7.0 MB (7005858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1899c13c410a0f6b97b115a976d5edf585c69deec937b4e307a96542b9b4b31`  
		Last Modified: Thu, 05 Sep 2024 08:05:40 GMT  
		Size: 16.0 KB (15976 bytes)  
		MIME: application/vnd.in-toto+json
