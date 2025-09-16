## `clojure:temurin-21-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:52ee84ab07586971a089c33fb20d10de8d2d1ad3f134ba952996ab7b81545c91
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

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:31e1efdb239979356a918488eee861bfa4a22a3f7831f679d87961793b00268d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259561769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a3ba6f9b58f7d0798537a546540a58a7c94aca37a7f003c9e5a79ad3632f1c1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45fd0137763775eb12248acb70b1b25c77d9e243f4337d5cffa03f4c493e98d9`  
		Last Modified: Tue, 16 Sep 2025 00:20:08 GMT  
		Size: 157.8 MB (157804768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c4852033006985ac2e4f58c468c256b900aa07f83af47c11f2062894868d896`  
		Last Modified: Tue, 16 Sep 2025 00:19:44 GMT  
		Size: 72.0 MB (71982465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adb944823f11ab17699903d8117417a236083c863b6cb71ea2d494d463136e3`  
		Last Modified: Tue, 16 Sep 2025 00:19:39 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba01ae87e8a2b4698a1083914ccbb193fdccda8f61ba9cda158d5da35fd15dc`  
		Last Modified: Tue, 16 Sep 2025 00:19:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9db5938a4fe98da4af572bbf46b2cbb3a2f673fb41bed89b7d4a60254d30ad1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0aa32891fe0899730db88ed6f77fb1dd52bb5562b0e0965fbff4de3c7575334`

```dockerfile
```

-	Layers:
	-	`sha256:ec2feb719b6a86c58fac6b611a57636646f7a75dc20211231d03bbd3819bcc2a`  
		Last Modified: Tue, 16 Sep 2025 00:43:51 GMT  
		Size: 5.3 MB (5259903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06de660eba223c06d0a64fd6bca52ea16b27a8d9f05ea77a55d55decd7041566`  
		Last Modified: Tue, 16 Sep 2025 00:43:52 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e801861919783206d26b101fd76953e4ad3df35b225b410c6ca07f8b1e661e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (258022800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3882b5fd1694b1853fabfbd409d5ffe5ab1230136d15ab53391c0183bf944f71`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec1f44e1d6c2f84180451dfc31c43a8130544d9cae3b1b834620d9d3776cd030`  
		Last Modified: Mon, 15 Sep 2025 23:28:09 GMT  
		Size: 156.1 MB (156081177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1de426bb4085a154966b5cc93b6d92c7372e5ca2182d61ee0bec979be50306`  
		Last Modified: Tue, 16 Sep 2025 00:34:56 GMT  
		Size: 71.8 MB (71803950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7d5810d664115846c43cbf7e77a8ee0148fa738e81d86fae139fd927cae795`  
		Last Modified: Tue, 16 Sep 2025 00:12:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6089c4b5b92a8f64a2c1441c72c7ff6f7d0de2071f5d2f10272969462424ddf3`  
		Last Modified: Tue, 16 Sep 2025 00:12:53 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:246ee1ce4abb4adaef8b0d3bdb155d79601b5bc24e24976d6b6a7c8d255f45a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5282381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0130b04173b285afb495435cf4d3f52fd2abd916dd3da6fe02938211c0a1ec45`

```dockerfile
```

-	Layers:
	-	`sha256:16d803b4b35fcde201c335aa83d6ba2bbc96f589f648ff2f4f11eea423847a25`  
		Last Modified: Tue, 16 Sep 2025 00:43:56 GMT  
		Size: 5.3 MB (5265696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7703416fda0c0e86d342c3491137036ca0fa5da4edc0ef9e267b68860848001e`  
		Last Modified: Tue, 16 Sep 2025 00:43:57 GMT  
		Size: 16.7 KB (16685 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e987e3abd293701d78b469af4d32d26355bdb4d368586e992ea8bec20682b190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.0 MB (268957084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487dd7b95fa6dd8cc5af44d34dea5e2b301dc1e22ecf66e70c0123ad6e7877ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961eb7ebf0035f6d398671677d350eb2f03bf73e15b167f039f8bd38980355b5`  
		Last Modified: Sat, 13 Sep 2025 03:48:15 GMT  
		Size: 158.0 MB (157963461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86ad77c71a41b3944da298a837c21bfb96767671a02218e67806537f9738f0f`  
		Last Modified: Tue, 16 Sep 2025 01:25:43 GMT  
		Size: 77.4 MB (77398229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2655ce2c482d0aed6901710ba68c335dd7f1f35b90e649c612f00a0308af04a1`  
		Last Modified: Tue, 16 Sep 2025 01:25:34 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92204d0398e1c671d038db49c114bcef0f34dececb6917374741479559ae1ea0`  
		Last Modified: Tue, 16 Sep 2025 01:25:34 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:10ddf15a18e518de08808afdc32aa6f9525a834a769db80c6e09ceccc3f44094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c24c10c2ec280e5587e92d2c073441c1f9c3c621a380a4ef5800f44f0481b7ce`

```dockerfile
```

-	Layers:
	-	`sha256:90c27a26b12ba9fff78fbd3a428d410a617b921a5fb2d6729b177199872378e5`  
		Last Modified: Tue, 16 Sep 2025 03:41:55 GMT  
		Size: 5.3 MB (5264286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e57883b032fc45cbfb98c0df2e813b99484461c7eec99c418ef8ae15adc616d`  
		Last Modified: Tue, 16 Sep 2025 03:41:56 GMT  
		Size: 16.6 KB (16603 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:441e3b3c954ee8248789566950010c98500b2d4729e15685c72a6e7accbe26cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.7 MB (252745815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320b6d0f3fb0347d795f0905ac43b9b33bcb00806004cf4e3bd081743f4c421d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dd4e3fb8766f676c414c0c55be0f5d9f6e6359dc2628caa804016b0f2ba461f2`  
		Last Modified: Tue, 09 Sep 2025 01:07:45 GMT  
		Size: 28.3 MB (28271372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25be0a32c196b5e86daa223045b0e32e55940405ffb33be6fe5f6bd48aeeeee`  
		Last Modified: Sun, 14 Sep 2025 19:26:07 GMT  
		Size: 153.6 MB (153593492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de8edfb047643d39d1a8eae5f97a87517988aad5024f669070bbdba01bd39b0`  
		Last Modified: Sun, 14 Sep 2025 19:26:14 GMT  
		Size: 70.9 MB (70879906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757f585b18e2130e580ffd8f796b8b506c887529dd3e482f7d5b5bcec5f4afb0`  
		Last Modified: Sun, 14 Sep 2025 00:30:23 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e6e75f238d5c12884d611331d2baa971d46ebe494d9abc8c46114b281d09bc`  
		Last Modified: Sun, 14 Sep 2025 00:30:26 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:128f7d66f1e936346fddcac20df81d22ae93d24dbb73c88e6871e19af7784018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5265982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d665230282d90060a5d55e6852c4fb7f7d7643c11b1b02f48f6a84410fd1429`

```dockerfile
```

-	Layers:
	-	`sha256:faa71eca617f2ac4e7a31245e64d8b8f225f7e2727b0ef094e7b0fd7dda5c63c`  
		Last Modified: Sun, 14 Sep 2025 03:36:11 GMT  
		Size: 5.2 MB (5249379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1eca6a38b24991ac47d97c16c025bd60740bac9082d2bedced6945e4067f9c`  
		Last Modified: Sun, 14 Sep 2025 03:36:11 GMT  
		Size: 16.6 KB (16603 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:6626b2d86c626044390fd864f06bcaf5eb1555ad9ab14e73e5799c5d233ee909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.8 MB (249812445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be074aa1985e4a4b30d98557f35472aad9c40b1f0d55eec6328ada514f43830a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
# Fri, 12 Sep 2025 20:29:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 12 Sep 2025 20:29:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Sep 2025 20:29:18 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Fri, 12 Sep 2025 20:29:18 GMT
WORKDIR /tmp
# Fri, 12 Sep 2025 20:29:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 12 Sep 2025 20:29:18 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 12 Sep 2025 20:29:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4c284aa571e77182f2d698660ed6e8ab6e5fbf5fa1bcbcf0017032e82225f4`  
		Last Modified: Fri, 12 Sep 2025 23:59:48 GMT  
		Size: 147.0 MB (147027059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df15222beef1e241e5667b2b51d3ea0f362dc9769b37aa9cfcca0d1943284e4`  
		Last Modified: Tue, 16 Sep 2025 00:57:58 GMT  
		Size: 73.0 MB (72951438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403fa097e97d41ca99347734798897e9c8efd3dc3a10978a806b5893bfb47bda`  
		Last Modified: Tue, 16 Sep 2025 01:43:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3ecdacfca9c24a4241acd5fb56015ab42aed3901cfe6531625794c74065d0d`  
		Last Modified: Tue, 16 Sep 2025 01:43:14 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:793059d3ad0f2f67aeb5097550b4efa515224927e9ec87a41f31f65a63fb6cc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e101d2c6b6d20be720f6fb2dd1b737dd9f7e7127403216c31e6fa267a3285a`

```dockerfile
```

-	Layers:
	-	`sha256:f6d3aff9caf7dd3c03735d2c74cdb6dc8735b60a653b68cbb9dd24a998d83085`  
		Last Modified: Tue, 16 Sep 2025 03:42:04 GMT  
		Size: 5.3 MB (5255827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6fb3cd7dfd4d9175bedccf6d132d96dc66ad6939dc78c6f49705dae7aa0abb5`  
		Last Modified: Tue, 16 Sep 2025 03:42:05 GMT  
		Size: 16.5 KB (16543 bytes)  
		MIME: application/vnd.in-toto+json
