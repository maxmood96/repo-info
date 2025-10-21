## `clojure:temurin-21-trixie`

```console
$ docker pull clojure@sha256:8c64664fbfb27f144f22bd753c28d225bba8a77644526692647e52de53327b3b
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

### `clojure:temurin-21-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:b479b399976911e99e4010d332c9758abbaf9d31c0d8539565f3f957b02dfcea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.6 MB (292632639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2051644fe4ac24a07c43923d019c93127567844fcbaf0842009b83a240865ba4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:795dbedde24d2c72dafd2b71fe36643552e56859c0e29cdb095ed54b825fbaa2`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 49.3 MB (49284971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051b084dffcc32737f3f7f01122fd6d83128ae86aa6165aa99896da9c5066521`  
		Last Modified: Tue, 21 Oct 2025 02:23:32 GMT  
		Size: 157.8 MB (157804769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4e5d4a17a0f83b586630d07d370d019111707008cf904c15637628e8b4bceb`  
		Last Modified: Tue, 21 Oct 2025 02:23:47 GMT  
		Size: 85.5 MB (85541857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29c94c2b7a8189728b719b4cd7745f4fef009411c761a5785da1fe352174d7b`  
		Last Modified: Tue, 21 Oct 2025 02:23:42 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f743efffb9c5dda54bacf89e067b9285f6a29091db53d8785e376ac686f0f34d`  
		Last Modified: Tue, 21 Oct 2025 02:23:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:28e04a978ec0baff777d21e9cb20442efa0e4ae8a0aaff8a0195d6b366bb888f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7485797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef417afe3e316f0d245d538a71b02306d0a8ccac29a986916d56db33412816b6`

```dockerfile
```

-	Layers:
	-	`sha256:05d2cf6bb47d3221ba2b19c47859658419d19c512b525bf106fd91572c50531c`  
		Last Modified: Tue, 21 Oct 2025 09:43:18 GMT  
		Size: 7.5 MB (7470001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b4c4f38e3b6642021293a4a3c4b7ec48ad2d7cf77c5b031b980522b27290e50`  
		Last Modified: Tue, 21 Oct 2025 09:43:19 GMT  
		Size: 15.8 KB (15796 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5a0fd381d2014697bc88417dbd22d4da0ca538c627f77645a51d0d5b8f64ed2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291094522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7ed3d81883f86cffab21d49061fe2bdab9b1476171a8b870ae43df18b8f54f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2a101b2fcb53d61db540cb76da094137d4f0291a93fa41357ab70c3debf4d3c3`  
		Last Modified: Tue, 21 Oct 2025 00:22:57 GMT  
		Size: 49.6 MB (49649743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0852d5f72a3da59c2b707b3b0c22d0bfbc3ea36bbc4a80120e2202045a022f3f`  
		Last Modified: Tue, 21 Oct 2025 02:29:10 GMT  
		Size: 156.1 MB (156081233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913482d624d49c986a165974f07892fcc2fa305cf4a3e1bf48574cc3efd4a641`  
		Last Modified: Tue, 21 Oct 2025 02:29:24 GMT  
		Size: 85.4 MB (85362507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b208bf7a7346e45c4c99c76000784fabb38b2b3812d1cf8fa086ec1b34b8d64`  
		Last Modified: Tue, 21 Oct 2025 02:29:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d866222fd3d3741774bd2927136770b3049628bcfdb71884e5121d4e5dbd95`  
		Last Modified: Tue, 21 Oct 2025 02:29:17 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:981564d4a36d7c286f07959fe42f5a395b565144f8567bb18aea8ff95a7b50fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0402f2ae1808069d8f85c4b844a2758b407a08de5b4d20ca2db1abae995a2a87`

```dockerfile
```

-	Layers:
	-	`sha256:8d226c97c9bde8b5c0037c9922c28e1160b8bd2afce51385fc5568af9fa2ad61`  
		Last Modified: Tue, 21 Oct 2025 09:43:24 GMT  
		Size: 7.5 MB (7477031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:996e105e55201ae42fbe02a1535bbd8ec7bd7b19584f4c53f0cff946c0e0f986`  
		Last Modified: Tue, 21 Oct 2025 09:43:25 GMT  
		Size: 15.9 KB (15915 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:ee5c9c977f36a1bf49342cd8f487e2e2ab68abe03c71e78f6571672548cd0bfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.2 MB (305225293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff20cd1441e53d28e93af21ede4e3070fd6d9e58c1a5791db098872f718398d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71fbf24a239310917388930bb043e64907cb532b9ac8f265e44e032dc3bf4409`  
		Last Modified: Mon, 29 Sep 2025 23:41:05 GMT  
		Size: 53.1 MB (53109217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bcc20bd317005af8d9991ad8ae6131f921e32b6786a4224aa1f30be15e3131`  
		Last Modified: Fri, 10 Oct 2025 21:32:26 GMT  
		Size: 158.0 MB (157963428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea6ff59d57723ae6b815a96561b7b387b3cb600e6bac90eaa123b29a547c9e9`  
		Last Modified: Fri, 10 Oct 2025 05:48:09 GMT  
		Size: 94.2 MB (94151604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30973d047272d1d6c3cf53777cb8963eb9def2fc5aedcca182e546cf8645fad2`  
		Last Modified: Fri, 10 Oct 2025 05:48:02 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94625716117ecfb1fe433692e755dd65a96ddc59596cea74b61b639024f538f`  
		Last Modified: Fri, 10 Oct 2025 05:48:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:460e228f272f5cf672ebe4a75eea3e7bfb07fd98adae3916f4dfedac7fc53fca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:127d26e555db820ec6e68494862a85040d801525f9629d3ccb3d22dc6ddaa000`

```dockerfile
```

-	Layers:
	-	`sha256:c5fe08397ddbd0f68dc33bfc86e9654fc199ee3848ae8f28abe58dd2132d94db`  
		Last Modified: Fri, 10 Oct 2025 06:46:33 GMT  
		Size: 7.5 MB (7474420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:661d2e02b5578e936c9bf4b89d666fcdb8837bc870071ab4ee07395761dce316`  
		Last Modified: Fri, 10 Oct 2025 06:46:34 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:16a0a73c438a7c4414dca128580a2032a7d3d4e5d8422c4ef554f98dd6338deb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288414015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7cef2141592ed24e8bb49f1b3e77d2f07bb8cecd2ec5bd0bf19b6934aa89fe`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:913254a25f5e448a50a1e74fa50f037e22f85cfe4d6a3c626f4b7405299b7c1b`  
		Last Modified: Tue, 30 Sep 2025 01:03:38 GMT  
		Size: 47.8 MB (47770009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce753221b06cbfd96d1f82257a8749e02e506fd9eb43abc94d8d907e213d7a23`  
		Last Modified: Thu, 16 Oct 2025 21:31:52 GMT  
		Size: 153.6 MB (153593526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ebd0775936c0558c0d2aa62fc7a932df718024280e9e3cb14fdceaa6c655dd2`  
		Last Modified: Thu, 16 Oct 2025 08:34:29 GMT  
		Size: 87.0 MB (87049436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20b7210d3d769cf0a11e0d42f20cc0d61cffd122029634586d553dcaad0390e`  
		Last Modified: Thu, 16 Oct 2025 08:34:24 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75cd803d2de2b005a898a3e927e512bd7b28dded0c7dba34db927311586e0579`  
		Last Modified: Thu, 16 Oct 2025 08:34:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3810e6a6f5548ae7081b27e6cb7f9f9e93811631280917984e824da5f33e09b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7473759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359a39014e770a3a6f8472c01cf965ae152c8db094546a1fd90dadd9a8aa3e1f`

```dockerfile
```

-	Layers:
	-	`sha256:6b91f4c8a1d534b1c5afe1f1df87e9a1084b6b2ad8d437b474e2437db83849d3`  
		Last Modified: Thu, 16 Oct 2025 09:38:36 GMT  
		Size: 7.5 MB (7457914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b01d82f5f3fafc1b7b819beaf6302ccb2bc1337d950fecd65d5d5e9d5244e959`  
		Last Modified: Thu, 16 Oct 2025 09:38:36 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:2d67ed9880de9f0194ee788594991b23cb6b947cc6f38cd4dec79882ba1c2dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.5 MB (285504371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87d15483bf62e526f00a28bbf2f145d9a50167d1bcce58d14a57f446da323e7a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:024d6c344f0b9dbb2baf07e95dfd2abbfadc5c8262ca381f39f6489670cbaff5`  
		Last Modified: Mon, 29 Sep 2025 23:41:06 GMT  
		Size: 49.4 MB (49351442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74df676eff8aac4cf4286d35670c399929547657319b92de6c69514bf176fedc`  
		Last Modified: Thu, 09 Oct 2025 23:28:35 GMT  
		Size: 147.0 MB (147026949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017a6113970bc58f0b0d39568a54cb3aeb1e286e296ea879f03ef4ce5ea73cbe`  
		Last Modified: Thu, 09 Oct 2025 23:35:13 GMT  
		Size: 89.1 MB (89124938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2a14ccd99da91215c696334de472e7606ac8dcb5077cc31267f0f02e2ecbe2`  
		Last Modified: Thu, 09 Oct 2025 23:35:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e27c150f0aee0ee2cacfc68d0e0e0b656824a2423fe9dbc5aa4533c241e78173`  
		Last Modified: Thu, 09 Oct 2025 23:35:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4e6c9c594ca0bb251309ebbae2385a9ce3e253110a1a9abf6c062a0cfd4f19dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7481720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35d5c39f9e1254fbc9717aa9917ed8fa3b9107d245ea7e719d4a7269cdbbdfdd`

```dockerfile
```

-	Layers:
	-	`sha256:824bdb295a89462a4ace46ed8e6038fbad55fa446e33833db5e6fc9f1f395a45`  
		Last Modified: Fri, 10 Oct 2025 03:38:05 GMT  
		Size: 7.5 MB (7465923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0780e87c3871d85d3d3c0c39c96f3d90413fe241a8603834d002940429e2358c`  
		Last Modified: Fri, 10 Oct 2025 03:38:06 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json
