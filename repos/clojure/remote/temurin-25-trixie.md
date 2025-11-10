## `clojure:temurin-25-trixie`

```console
$ docker pull clojure@sha256:13192f3cd9b542694587816b3ff21eedac888b52b596af693d81b94d088211ed
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

### `clojure:temurin-25-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:fcc9d288c858c7ded1cb946c72f1b05124101e00a0ba85200f69d3eb80b5d746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226872706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d77df0425d2dae155b250ccd68c8b55434a19d6b4002a93181cb799ff66fa3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:46:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:46:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:46:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:46:21 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:46:21 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:46:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:46:38 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:46:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:46:38 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:46:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4255b5aea3664272bf185592030fa690a02fd4cbeb13ab1525f76a3b57d002e7`  
		Last Modified: Sat, 08 Nov 2025 18:47:19 GMT  
		Size: 92.0 MB (92045299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31133e9de921ff1dd2c785f63bafb70d2e2a9da840b03b22b3b593a5d389f91c`  
		Last Modified: Sat, 08 Nov 2025 18:47:34 GMT  
		Size: 85.5 MB (85540732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3fe1024cce4fe67e3eb24421662f4c5ae8f71532fabbfb8050cd8a50df82f3`  
		Last Modified: Sat, 08 Nov 2025 18:47:16 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa04215bf740d510a5c9d044c80cb67ccd95239eab897f5ca0e759049fd39ad`  
		Last Modified: Sat, 08 Nov 2025 18:47:17 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4968fcc3a9598a3da8215d9334bdef68a98f7a430710a9114eed186782adf796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a3d61f18b68eb4a6b363f4ab6e9e087fbdf70122daac193840793ac7561f38`

```dockerfile
```

-	Layers:
	-	`sha256:9c826a9d9bc005dd954d0e1d839ef8aae0691157d8fa142bac9af3ca60151e73`  
		Last Modified: Sat, 08 Nov 2025 22:53:17 GMT  
		Size: 7.4 MB (7418231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a64ce6ce55ddce8e71539f48e8e5d735f67aadcad33386ef0c17f022eb1134b`  
		Last Modified: Sat, 08 Nov 2025 22:53:18 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8ed62b42ad6f7b4ea338f5d8471636889ca6a155410b9d5cd83ae87ed1022489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226067266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef74d3fa27faf9e782c0b895235aeb0f51658d2f69884b05bf0e9dc025ce8b5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:45:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:45:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:45:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:45:53 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:45:53 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:46:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:46:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:46:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:46:12 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:46:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfff61ee6d95b0b04626a7242ebd016a940a2796dc443f3a1b6f29901e7f4c79`  
		Last Modified: Sat, 08 Nov 2025 18:47:02 GMT  
		Size: 91.1 MB (91052530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ab6d9da03f0aa4df045f293793fdb0bc52948b41eb1c1a5e46e225df91dd28`  
		Last Modified: Sat, 08 Nov 2025 18:46:49 GMT  
		Size: 85.4 MB (85363262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cfbd7f9d616b63d2b9692a476e0daca239fc7ac968489d5c913ff6ba502e94`  
		Last Modified: Sat, 08 Nov 2025 18:46:42 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050c37f687b2a27482b72004113f09ea63e835ce42e92b31e693575c15b79410`  
		Last Modified: Sat, 08 Nov 2025 18:46:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5bb10240f9a0fb19ac3f19de79da332155ea689360dce53e2e4c319adab7977a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc8edb615dcf7c209b6434d6e3d222b743b8b88727186c555c8da0a69d7d415e`

```dockerfile
```

-	Layers:
	-	`sha256:ae91c5af205a7317850f652ebf174d5c15ca700f63cdab842e8e509d4d169859`  
		Last Modified: Sat, 08 Nov 2025 19:37:23 GMT  
		Size: 7.4 MB (7425282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfd83b481eed255b02ffbc41f6521ef46ee764cda9be11e2d5f357a0abd73c1a`  
		Last Modified: Sat, 08 Nov 2025 19:37:24 GMT  
		Size: 16.6 KB (16557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:6546def60c80d9adf8d79450c42594a8990cfc3ac20dabe02a80425732b4700e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235671984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768a41ad1e0809b59b30cf0cc4f65d45dbda2dffddda208294c126282c847f02`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 21:49:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:49:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:49:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:49:21 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 21:49:22 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:57:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 21:57:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 21:57:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:57:54 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:57:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:446565adb94c3c0ddf2d551f99efb1cdfcd6ea440c7b05bac7b6b03d99ddeddd`  
		Last Modified: Sat, 08 Nov 2025 21:50:56 GMT  
		Size: 91.6 MB (91610756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471108546f957de3c053e48d3b48aedcdeda97cfce9d57cddd103c4f1e8e8490`  
		Last Modified: Sat, 08 Nov 2025 21:58:50 GMT  
		Size: 91.0 MB (90950058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85695fdb8df2b9bec2a5318896609179ac35898551c2600069ebaeb2b5996f3b`  
		Last Modified: Sat, 08 Nov 2025 21:58:45 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e8403c03940ed0ba5ef3812f2f00ba8dcac701bb0907bdc4dad0e539cc801`  
		Last Modified: Sat, 08 Nov 2025 21:58:45 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:23ee80680b8ba12ccac2d9c87327e7b7d9f7386797fa0cf0adf0c3e920667d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf2e8e6a148d7dc6912a74cdc7efaa61e4a2da3ace8f249005aa48a1a05b1e0`

```dockerfile
```

-	Layers:
	-	`sha256:6508f6deda5c330c2397130d8bca27365b65d3e6a458bdf6eacda8eca5c79c74`  
		Last Modified: Sat, 08 Nov 2025 22:53:28 GMT  
		Size: 7.4 MB (7423960 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a2d1e3e5155dbebbb1e267366e36863db4a74c68ec07c85eed9b2d5c9228541`  
		Last Modified: Sat, 08 Nov 2025 22:53:28 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:ff157b141966f98c8237a04d2c99097f4c5458280a8090665c3985c756c2ec64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222951611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cc0d28a5c36e22d4f1da2d95713f4f69387199dd1bdc6899443a78e8359ebb4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Mon, 10 Nov 2025 04:31:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 04:31:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 10 Nov 2025 04:31:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 04:31:34 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 10 Nov 2025 04:31:34 GMT
WORKDIR /tmp
# Mon, 10 Nov 2025 04:52:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 10 Nov 2025 04:52:16 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 10 Nov 2025 04:52:16 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 10 Nov 2025 04:52:16 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 10 Nov 2025 04:52:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:de6b66e2abcf55248485e438d6def9b92cf28773b7cd7896ee78f9409b6e7526`  
		Last Modified: Tue, 04 Nov 2025 00:27:48 GMT  
		Size: 47.8 MB (47770924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce920aff3ffeaa315b37b62cd44c0edec347fdf6332b121c2409c04bb3cf227`  
		Last Modified: Mon, 10 Nov 2025 04:37:22 GMT  
		Size: 90.8 MB (90752887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9c3728cfa212089d143533a0fa21dc32bfdfbfd6f464a5c0ab401abccabd28`  
		Last Modified: Mon, 10 Nov 2025 04:56:46 GMT  
		Size: 84.4 MB (84426755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e1e1ea7e27661ff0e5ae8f4a303182e008a76d7883e12f9e97c283159212c4`  
		Last Modified: Mon, 10 Nov 2025 04:56:38 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7463f69382d187ee06ae494fd7b0dfdd5f5acdae7f40187cd7374467ae2b1cb8`  
		Last Modified: Mon, 10 Nov 2025 04:56:38 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d0254dc340c8115d89bf7b60ee88c2c29bfdc3085fc154696bcf86b44fc8578a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7422628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6598325a0dfef71d2636c093f1c48953e58dd1c09991146f5c750a79b95b1a`

```dockerfile
```

-	Layers:
	-	`sha256:33b41c38317cc5426cb6aa05dd6f28ba482614cc5a08294733ca6f674464c909`  
		Last Modified: Mon, 10 Nov 2025 07:38:05 GMT  
		Size: 7.4 MB (7406153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be96c285c1edada14ea775bde9713df21b05cc644ddb80ed2377dbe2b21dfc13`  
		Last Modified: Mon, 10 Nov 2025 07:38:06 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:8358d6f92afd7c83c68659043acaa5bcdd5c576fce9fccb2079ebf7fb990fe15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224071875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0bcbe836106364c6592b10d681437712199ec934c7a546feb0c014d1207481`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 20:39:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 20:39:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 20:39:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 20:39:14 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 20:39:14 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 20:44:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 20:44:35 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 20:44:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 20:44:36 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 20:44:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b03eddb65d5a7688f7d8e1526982f728fe30afaeb85c4393004d80fa599ab55`  
		Last Modified: Sat, 08 Nov 2025 20:40:05 GMT  
		Size: 88.2 MB (88210741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52bcd2a29dd774d582955b31cc1ed93508247379914a4bb5ed5f28c9bfc0f22a`  
		Last Modified: Sat, 08 Nov 2025 20:45:11 GMT  
		Size: 86.5 MB (86507791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235593b3862ecda4159d4c62db33d1acc7d56d0fc36a0719e328ea1254951a5e`  
		Last Modified: Sat, 08 Nov 2025 20:45:06 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ced86508ab17a3558e55f0cee18b16016f40686a16fabd64fb7ba5a9f13468`  
		Last Modified: Sat, 08 Nov 2025 20:45:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5ad04f9bad3b49158f50245c29d3f1cbc495c1addbe0bc3a8a3099c4ca8e8a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25de284f0f30c93741ce37587f865396ec0f3c1ab33ee692ba24c0cdadc17468`

```dockerfile
```

-	Layers:
	-	`sha256:f91e8255a7e700641ec28f1ea08847d856ff2efebc4b6ba38c38093cc8ee5f95`  
		Last Modified: Sat, 08 Nov 2025 22:53:39 GMT  
		Size: 7.4 MB (7416701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9befdc6ee5fc40d85e82c21d959dd82edfccf2302c469b8eeeb9b0293e93c9c`  
		Last Modified: Sat, 08 Nov 2025 22:53:39 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json
