## `clojure:temurin-21-tools-deps-trixie`

```console
$ docker pull clojure@sha256:0be663480241025af765e830a8fe05634330a8c2bf8f80ef35c273a5945ffba7
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
$ docker pull clojure@sha256:13810cf10face1d24e597412e0f1eb2f58f040fb08244acb896114eb2846cda5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.6 MB (295588875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d21f5c1125cedaf7b8437d29ffafeca934a1a8443cc4c29cd90c68448f52295b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
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
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e7363fa6931c7b2a3f1eba14ee32e03e5723919637c7708f4741ef5e5017b8`  
		Last Modified: Fri, 10 Oct 2025 09:38:52 GMT  
		Size: 157.8 MB (157804769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a365977e9173b5858e57dd297de91858120065952713201b5086cd51773c27`  
		Last Modified: Fri, 10 Oct 2025 03:57:11 GMT  
		Size: 88.5 MB (88498437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e03458270be9a92f5a278b3e7d027d538acf1350af827c6435a2bdcdb42cd68`  
		Last Modified: Thu, 09 Oct 2025 23:13:23 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24465017bb07615b2873a8052deeff9cacc9a6514d5539a28701479405fe603`  
		Last Modified: Thu, 09 Oct 2025 23:13:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:9ce06243e860d1b983ac63c578db7b22d5e6da21acd9893a9fcbab4ded61f32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7485798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c88c1f5838d6eee34f05d7bbb3643a3355f128d6bee142db5eabc7dffb36ce`

```dockerfile
```

-	Layers:
	-	`sha256:70567c685622213de2b0205e579cd52f3b76ed91bfc8bb677e481d887478a03e`  
		Last Modified: Fri, 10 Oct 2025 06:46:18 GMT  
		Size: 7.5 MB (7470001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:978b1f4c00609677a8ddc0392687d183de875634e4c4354bfec6ce1ee96240ea`  
		Last Modified: Fri, 10 Oct 2025 06:46:19 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:15227015e690d25ac14c722c4c25d0d66b10f7002fb49d1efd0c049eef9af5c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.4 MB (294421326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5520bec423168b6be67f0a2bc5ae0b508fc1de0b69dc3f0dc64cfe2da192ea53`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
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
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fca3a7e95af1f37e3ac44acf105a07bf47a3b21f683167cfac4c50fd855bee7`  
		Last Modified: Sat, 11 Oct 2025 02:50:20 GMT  
		Size: 156.1 MB (156081207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3963de65783f6bf7415dd4d2b964fe97dc4a41f1c381ed490bf5f3326beb3234`  
		Last Modified: Thu, 09 Oct 2025 22:30:27 GMT  
		Size: 88.7 MB (88690383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea41a1beeb09d0f7737095dfeb5d133f563486c3643ac2043b04134bbe337ed`  
		Last Modified: Thu, 09 Oct 2025 22:30:21 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45453e8856778376a4964b4fde44d684a8612b7a40bb4ab93ad5cac5ced65d9c`  
		Last Modified: Thu, 09 Oct 2025 22:30:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:55d518f1e073296d4b2b02b616c0cb770cde42d3ac0a57954f291c2dd98f1bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9262fb243560ef3dff877e2c86eedde101b1b6e46b68f4483b4ef668ea17e42a`

```dockerfile
```

-	Layers:
	-	`sha256:e398f9dd56ad755ee3c123e08528ea657f9894c06d37c5b0f902efa67f6e71c3`  
		Last Modified: Fri, 10 Oct 2025 06:46:26 GMT  
		Size: 7.5 MB (7477031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ef99df30ac6ce85e76efeb6cff97223413f0f22480d86d68bc67105c509f3c4`  
		Last Modified: Fri, 10 Oct 2025 06:46:27 GMT  
		Size: 15.9 KB (15915 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; ppc64le

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

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-trixie` - linux; riscv64

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

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-trixie` - linux; s390x

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

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

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
