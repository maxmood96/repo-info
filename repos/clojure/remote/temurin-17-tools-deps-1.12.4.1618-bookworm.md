## `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm`

```console
$ docker pull clojure@sha256:ad1faf90a528a799fe9dfa65bd397430f8a433097e3e2230739a273cdd4a8538
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

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:5c057a4c2adeb9d7d680cfe9bbb87ad517742f82ce62767ad4bd57268957383c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.6 MB (275561740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6368dfc277ff8ee55478aa6a7c588a36fca8b56eeb2a6bfd91c7a89de4d060b1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:07:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:07:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:07:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:07:48 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:07:48 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:08:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:08:01 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:08:01 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:08:01 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:08:01 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1808410e63d1fd301c755c86b1af7155108cf80a1221a16396bf7d0260034d1`  
		Last Modified: Fri, 08 May 2026 00:08:28 GMT  
		Size: 145.9 MB (145905478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a843d48280770a14924387f154a23bb4178bbffd9dbc1c6c271808b1efbd291a`  
		Last Modified: Fri, 08 May 2026 00:08:22 GMT  
		Size: 81.2 MB (81166595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:846ba22872af815ebe88bd7c4141823e589fdf9045e95a38cf6d5ec9ca04fcfa`  
		Last Modified: Fri, 08 May 2026 00:08:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8340527da2edea667c09b9ba355bfc8afa6ee9781f7e72107d8ff2c9e80621ca`  
		Last Modified: Fri, 08 May 2026 00:08:18 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fe81fc46a50475a9f286d8df01ca68278f7fff327bfcbbe51cf8c42fc02fce37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7394859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a63aa04ed5ab9df4fe320d24cdfb2ba457a9c9eb951b7fad1c65112ba0e0f9c3`

```dockerfile
```

-	Layers:
	-	`sha256:d5591a85dd5cea6916848683f0e2bfb1fea28c07366a56c60702702a8f1fa95f`  
		Last Modified: Fri, 08 May 2026 00:08:19 GMT  
		Size: 7.4 MB (7378929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:123f747bd2d46c05e46a6bae9251d88c7dbe1444aa19059efeb28106c98f0043`  
		Last Modified: Fri, 08 May 2026 00:08:18 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aca18922ab786dbc7e92677e2ecc3e6ca2e87c8cbb03dcbc2be14815fb8c62bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274272501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bc329fb882965ed16bb985d1aa890a172ff85713ec6114ba5d1696c273b393f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:08:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:08:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:08:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:08:36 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:08:36 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:09:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:09:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:09:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:09:32 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:09:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2afb7290c6f0e6371103c0b0b34522435a82cd734fa3aa911fc15187c6ee982`  
		Last Modified: Fri, 08 May 2026 00:09:10 GMT  
		Size: 144.7 MB (144724305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8891b713b4a123a8adb1ec3f1be30875e797027b38f6071b50d5439401fac2`  
		Last Modified: Fri, 08 May 2026 00:09:51 GMT  
		Size: 81.2 MB (81174089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698cfab61028cab0bd20f82f16a86f04c59f73925306ba29e338c6dca6fa57ae`  
		Last Modified: Fri, 08 May 2026 00:09:49 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357eb92016a3053084b64ef13cbba640e7257c83ec33fd2b8b2db849118d9328`  
		Last Modified: Fri, 08 May 2026 00:09:49 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:44856406acf875952b98000e1c45ea11a3d8508f5e1f94beb2f7108cfb816d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488f6bffaa8d09ddabc6e0149e681bbef88e75075948bccc361aab69936b74c0`

```dockerfile
```

-	Layers:
	-	`sha256:d9e55054ce723db0342a80b4de3b2d5e0b50366f09aa0efda0e0d6f59f9273b5`  
		Last Modified: Fri, 08 May 2026 00:09:50 GMT  
		Size: 7.4 MB (7384692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0b61afc3139fb3b2d2a212dd14f4e221f6094f9dc1ca6e664cd23c7a0d7ab07`  
		Last Modified: Fri, 08 May 2026 00:09:49 GMT  
		Size: 16.1 KB (16050 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:2a074e76ea7dd7ac2f598b120a5a697b683323c88586b2b843ce8011d9834fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285107930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6cbcd34ec923f423294e2a6b5dfabaf9eaa183077b8e2956390cc99211e8f93`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:43:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:43:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:43:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:43:06 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:43:06 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:50:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:50:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:50:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:50:10 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:50:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1a630844f3ca330b4aeb3cf62ea83634554dfbe591d28cdf3d1bbe7c2c4aa2`  
		Last Modified: Fri, 08 May 2026 00:44:30 GMT  
		Size: 145.8 MB (145766245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0272ba3b63e5a8f5e8bc52fe20cea12d57aa685e78e0ed0e8af00c60cf28a963`  
		Last Modified: Fri, 08 May 2026 00:50:55 GMT  
		Size: 87.0 MB (87003907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8215814d5f034ca2952a3e5c8298434992e841ee59976199e6e4ac860f01ebb0`  
		Last Modified: Fri, 08 May 2026 00:50:48 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:849cb1872f7a7b6040e25b46cafa38b3836f868c0bd8fe727e87e93b4a6b9bdc`  
		Last Modified: Fri, 08 May 2026 00:50:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:96204f32aa781fc50bfa1dcdc2fd0dc7486a4c99fe31a15bc2258d171ae2da44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0927093711b6dbf7ab5453ee99118f302728b18945324ab988c78d5e37ffba2`

```dockerfile
```

-	Layers:
	-	`sha256:395e89d7e8bf9a56feb11fea8e110fa5c94e92e19dece86398df4ce1372629e6`  
		Last Modified: Fri, 08 May 2026 00:50:48 GMT  
		Size: 7.4 MB (7384145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:273914722ce0d7618af61988c0d9814377953869148993433dfd00161d80bfe2`  
		Last Modified: Fri, 08 May 2026 00:50:48 GMT  
		Size: 16.0 KB (15980 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:1a5d36b76501b557249b116a14433cc55eb121036c76294d10ceb964561ea0af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (263039030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8477d2051ebf118a7573c6729c8e900fd73409cef3285c1ada93ecfd4c701b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Fri, 08 May 2026 00:29:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 08 May 2026 00:29:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 08 May 2026 00:29:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 May 2026 00:29:48 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 08 May 2026 00:29:48 GMT
WORKDIR /tmp
# Fri, 08 May 2026 00:30:02 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 08 May 2026 00:30:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 08 May 2026 00:30:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 08 May 2026 00:30:02 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 08 May 2026 00:30:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38206bb588645d2131fc628f62819d53d525cf84aaf10e0559b10f1a7f342112`  
		Last Modified: Fri, 08 May 2026 00:30:32 GMT  
		Size: 135.9 MB (135910436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e4fa87b6360c4f1b024e38960c7d1c7f658179b0b951db2c565e1f36bee0bf`  
		Last Modified: Fri, 08 May 2026 00:30:31 GMT  
		Size: 80.0 MB (79979583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd71dabe189f4bc5e84cc3a10d6352133a854371ffdaeaac2d0e6441fa190d29`  
		Last Modified: Fri, 08 May 2026 00:30:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790bd3a5c6f103d77357d1c7777993cc7b91a011d89411897d09e4915bcc61a8`  
		Last Modified: Fri, 08 May 2026 00:30:29 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:6dc4ef06ad5291eda45f0c4e2ae17dbc8e0fe0a43ad26c73c5764de530027233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7386180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a856bc6057242bd84ddcff9cf9faed73831b8a7e5d4b2c6729999a7f6a0c295e`

```dockerfile
```

-	Layers:
	-	`sha256:a3611e654ec580634b2e73a17cd5acedb4eefb4b138351d1ced12a3a3b181f5c`  
		Last Modified: Fri, 08 May 2026 00:30:30 GMT  
		Size: 7.4 MB (7370248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33e94e8a95ace687633c255477123b29fadbec83140a898e846d0320e6b89bbd`  
		Last Modified: Fri, 08 May 2026 00:30:29 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json
