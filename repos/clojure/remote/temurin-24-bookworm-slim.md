## `clojure:temurin-24-bookworm-slim`

```console
$ docker pull clojure@sha256:fe8b528c2dbb6c818f881e10ad9cfb8054911a95397d98fc41f85fc2aeade8f6
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

### `clojure:temurin-24-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a0cab5478da228848b7e8e851d9007b9c2e8d534778f864c1f7da11efac90ff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187882610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5573af2bbded5d5f93132dac595b13d4a222555d60e02a5f772b62f36b12d206`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4523e9e3722efc5b73d45182cab571c837965727456bd2445de34422201b68`  
		Last Modified: Tue, 02 Sep 2025 00:18:12 GMT  
		Size: 90.0 MB (89975181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dc944690f4043a4b4972ddae4b33174c41fc27d2256a4aa813fbc4b000702af`  
		Last Modified: Tue, 02 Sep 2025 00:18:12 GMT  
		Size: 69.7 MB (69676132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988710f6326741d5716841cfc38d9844b31c5f41aed3ab4cf8833f1a067c0147`  
		Last Modified: Tue, 02 Sep 2025 00:55:52 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:084a051c915ce9b6d85bc840a9e89d27e5b38f894dcc99cbc6a2a553f6318595`  
		Last Modified: Tue, 02 Sep 2025 00:55:52 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:32efa620f998abecf5717edc22ec9d1935cec288a2442d72f3256a4e19c7a162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5077793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35494605208658d845f39ace68c847db8785247230aa668fd5bcaa71e63af24f`

```dockerfile
```

-	Layers:
	-	`sha256:9209a68336ae6045f6fc1793193023b87c7ae02c63459cf85982397096f3a817`  
		Last Modified: Tue, 02 Sep 2025 03:43:08 GMT  
		Size: 5.1 MB (5061921 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3840d25b35b89ea81fd3755210298d43f95e92526acbb17728401bc526ba7ef2`  
		Last Modified: Tue, 02 Sep 2025 03:43:08 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9b550d3df6bf18e0a824b241aa3a231114ded00621082a7bc378625f5b6bb625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186725040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef11cff56acd88b2a8f84079fb12e251f89c2c4634977013b0f138fe323cf4f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87e6bfd40fe1f401c5b893a66ab4775a180924c4ca26ac82e4428bc83ebf62e`  
		Last Modified: Mon, 18 Aug 2025 17:21:15 GMT  
		Size: 89.1 MB (89092530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f7975630abfe129c003e6161941bf52aa7975c07d762c097b2a02847dc605e`  
		Last Modified: Tue, 26 Aug 2025 17:55:30 GMT  
		Size: 69.5 MB (69549465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a760f22733f743d3feb36473008c7db3808d576f4cfb179090fcdeae8443f55`  
		Last Modified: Tue, 26 Aug 2025 17:55:15 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0013c0b9c120b51edcdaf70952bb17792dfe4d8af53a7059fa91dd9e0cff4b84`  
		Last Modified: Tue, 26 Aug 2025 17:55:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:93c25a85aea89169cc70d109029e833fceb902cf44e7fceb8719c4da47737dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5083669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e41d9f57562b47f9538124452d46a8d601404e08ee39cfef27919a1d781ef3aa`

```dockerfile
```

-	Layers:
	-	`sha256:91a759407031bd9dd5fdf66f1993a3d9ef5e3a46c58ceb60b213e499e5421bf2`  
		Last Modified: Tue, 26 Aug 2025 18:42:04 GMT  
		Size: 5.1 MB (5067679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ea083b9c594907ed7e2bd97449fce318a10e329e683dd41e95fec693f38924`  
		Last Modified: Tue, 26 Aug 2025 18:42:05 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d5c375848fe243c4066f05024fb52776845264e1324d8d49ad07458d1e4097eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.5 MB (197496935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f87ba8af2b04fe470aacdb38e5a68371031149b417587b78e21c5316f86ae1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72057f440526db0265c67512fdb1713f87ba9913daf842bcb2fc8b89526344fe`  
		Last Modified: Mon, 18 Aug 2025 17:37:14 GMT  
		Size: 89.9 MB (89918259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feba2215bde9ff4c6ff5aa05c0c6a007a7e6e44eceb705b742ff036fe56a44a3`  
		Last Modified: Tue, 26 Aug 2025 18:18:26 GMT  
		Size: 75.5 MB (75504209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371af8f38b46a0aa3865b4f7cf773f9529f079739d68e54784ab2ddcabd06cba`  
		Last Modified: Tue, 26 Aug 2025 18:18:17 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9253f18e8072fa51fc27c6191071803913e5208800853cf5f9815c90de4ecae`  
		Last Modified: Tue, 26 Aug 2025 18:18:18 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c8ca4a3542c5e7ac0d4940e9be08037ad0428c007041259ff6331611b457a5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5084297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:838f3008bee39998e85f6fd7bbfd68adb0c50ab74b9ff49be1ab633a3d095b90`

```dockerfile
```

-	Layers:
	-	`sha256:f79cd70f789585e2785d92169badba3cb8cef8b6b7226ad6735d943cc967f9c3`  
		Last Modified: Tue, 26 Aug 2025 21:38:12 GMT  
		Size: 5.1 MB (5068377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9109d3a7fe1e7482a63024a232b1f4ba46615dc809657600987af86f11a7e552`  
		Last Modified: Tue, 26 Aug 2025 21:38:13 GMT  
		Size: 15.9 KB (15920 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:8a5ae5f9b7de45a25e44add05975436d8069fdc9d1d0e9e5954f3f8e15203b67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180599560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e227ff1fcf24ed0d36e642513ea71b2a1426443bfa94f835a95cdef83657d0af`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c90ed0d6d56789641548c64b4a5818c4522e9490cd8bb164dce084d4e85b68`  
		Last Modified: Tue, 02 Sep 2025 02:22:19 GMT  
		Size: 85.2 MB (85226322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97641382c5cc646516da46a5f5885283486feec52e1bf33ff46fb853be502794`  
		Last Modified: Tue, 02 Sep 2025 02:27:12 GMT  
		Size: 68.5 MB (68484358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41981f93187ba14d4dd2c9041cb35e25fafa185f9147ef496d3e6f588cc1f47f`  
		Last Modified: Tue, 02 Sep 2025 02:27:06 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c329479e4c3601c2d0fe48ab1f2e30bccc53219a879e01b880a7978513379435`  
		Last Modified: Tue, 02 Sep 2025 02:27:07 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8bc7d48dbc39feb8fb7199764d01526adf089b337bcc54608409e7a318e14596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5071661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634ae29bf527a1648aa59c9494d2321b3f9bc605e8953154f812af1b32924212`

```dockerfile
```

-	Layers:
	-	`sha256:c66f06b05c32a63484f630ad36376bb4c3811937cfe0a972e77cd445b94cd586`  
		Last Modified: Tue, 02 Sep 2025 03:43:21 GMT  
		Size: 5.1 MB (5055790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04080c3e211fc58168494de211d97d4c12168ae9c7af19003beb00a7d3a5a7a0`  
		Last Modified: Tue, 02 Sep 2025 03:43:22 GMT  
		Size: 15.9 KB (15871 bytes)  
		MIME: application/vnd.in-toto+json
