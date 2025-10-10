## `clojure:temurin-21-tools-deps-trixie`

```console
$ docker pull clojure@sha256:d575456f50e354635d9ee3f87b43e393d3951e943b950e911ec46098e7a4fe5e
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
$ docker pull clojure@sha256:d5b6a2ec9a181f90f984076a48d171952e128ed0f41bb1fd0f15d6bece8def60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.6 MB (295588872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f600ff51e40d3ff12f3d7b45989a1cb119cb781e7a2855c48ef53118915a821`
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
	-	`sha256:ceb7e7c454872f8d08924a431664bd9ffa8accf869e844b3295a06ceb0f27240`  
		Last Modified: Thu, 02 Oct 2025 17:29:37 GMT  
		Size: 157.8 MB (157804773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3bb6de3c9cd816865f7f82c0050c832df2cc1501d11768e892a69c15546a9f0`  
		Last Modified: Thu, 02 Oct 2025 17:29:36 GMT  
		Size: 88.5 MB (88498432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ab066a27c64e2c7731f5bb3fe08f85a53c00ba3f46613ba54373a281aa55e7`  
		Last Modified: Thu, 02 Oct 2025 09:00:59 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5e8c7292364f0a65b05a9fbd2fd5f0c1d2a5b6fd3e7ffcbf899b702daf884b`  
		Last Modified: Thu, 02 Oct 2025 09:00:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c4148aa582932cab4226e116122463e7eaccc5aec03edecbe4649d59784a890f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7485798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff7b610f7c8f03843bb95347f42b13411ad11aad06b53bf402d7d3cf703b91dd`

```dockerfile
```

-	Layers:
	-	`sha256:7c350ea3f36ea9ac6dfa7700222bc38f780f10e956de508df2a77518708d2bf1`  
		Last Modified: Thu, 02 Oct 2025 12:43:15 GMT  
		Size: 7.5 MB (7470001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df2b02f132c98ba75485f546f571c1480175abfe2914180692b64cd9f34c74e0`  
		Last Modified: Thu, 02 Oct 2025 12:43:16 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c5d9e342560296c918738fcc1bb7674d2826679c8a5ed5815afe187fb1bb01ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.4 MB (294421569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c58f739b9efa116657a06e3e5f9e3a77d7b753e0b9d097c5979023ae9104f01`
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
	-	`sha256:d7c71fc27b3b52869ec8eed570f304367f7de8f596bf195cad368294135a0b18`  
		Last Modified: Thu, 02 Oct 2025 19:16:51 GMT  
		Size: 156.1 MB (156081248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46244bd7097d52e45886b2445e4f17537ea0c7e9b9d857830eadd4c70a95873`  
		Last Modified: Fri, 03 Oct 2025 07:29:25 GMT  
		Size: 88.7 MB (88690586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afe3d6d452326b6e172c927a218729bcdc8064cce1949f35b8c2145019af40c`  
		Last Modified: Fri, 03 Oct 2025 07:29:21 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc18ded0b1299fd709af2dc2efd1caf89cb7bf178a2a9a6231d32b0224895213`  
		Last Modified: Fri, 03 Oct 2025 07:29:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b63239bb40543d6a26a01da1f09fec2aec381b79cbae0449c1c8f3a035afc511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b13b2beceaaf2038d6093718c0bbaa2e3e48705be9aaa4be9666d155df8a36`

```dockerfile
```

-	Layers:
	-	`sha256:33c3fd08b8ae7f727f504db88a776c37dfabf746663ed8104b1ac5becf263e2c`  
		Last Modified: Thu, 02 Oct 2025 06:45:13 GMT  
		Size: 7.5 MB (7477031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0db25d7d9d1811a2fc323fc7f35b24fbe35537a1a4b10cad8bf09b95e51ff0dc`  
		Last Modified: Thu, 02 Oct 2025 06:45:13 GMT  
		Size: 15.9 KB (15914 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:32c160d2d0b399e78421503d2487cc826aeb82c6c5272d4bcbff29ab233eaca2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.2 MB (305225172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18503184f21c874eaa752194f6e0d7f0c080333390fd15f8ccd65271862c7113`
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
	-	`sha256:3afefdb7cd362cfb5b5757a4e17654e16446aa9f5eb9d1d34e733939619f04a1`  
		Last Modified: Thu, 02 Oct 2025 10:10:39 GMT  
		Size: 158.0 MB (157963428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f1bec41abdaabcc4cfcf28e1ca2531bdd6eea2410d8bb6900a6423fc254307`  
		Last Modified: Thu, 02 Oct 2025 09:28:11 GMT  
		Size: 94.2 MB (94151486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7fd925cbe9bc3622c542c6848854ba213bed43affcf4d3b16833ca1904d0cc`  
		Last Modified: Thu, 02 Oct 2025 09:28:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d28424a00b8dac3a500b1f78d08c30b4bcf7b9ee1d5cf4c2cb6011c9b3f5e3`  
		Last Modified: Thu, 02 Oct 2025 09:28:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:22c177c4b8ec8c1d25c00769b5fcd78633da967cca1b84d272cef440d3a84b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d18ebe353a1375962b4b52146a72719cd74bd95a2357c23ab4246bf79af663a`

```dockerfile
```

-	Layers:
	-	`sha256:78e0fa652479415488ff9785cea81eb7462d1cdeea8d5528a3d35c42be1b4224`  
		Last Modified: Thu, 02 Oct 2025 12:43:25 GMT  
		Size: 7.5 MB (7474420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea64073ee37c6fba22b3510805db6a3fd045a6fa33a5caf6530c6c3967206b00`  
		Last Modified: Thu, 02 Oct 2025 12:43:25 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:3a27307fb148d35b1eb7536d4303bb0747c099e8c39e372bedfe98ddb0110053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288413529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5b7ebbae631c5f6a8c53adfcba8dc3df97c0fd549fec254d4ce540cca07bc0`
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
	-	`sha256:868b21eab689108f7f29ce1b0e66e8173a0d2514e8d89a99a3e3442e6ce7ffc5`  
		Last Modified: Sat, 04 Oct 2025 20:48:03 GMT  
		Size: 153.6 MB (153593448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a41708016042fbd8b1a2617416a64b84c292a8eef28ec593ffd627b26d71ec`  
		Last Modified: Sat, 04 Oct 2025 14:50:26 GMT  
		Size: 87.0 MB (87049030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ccc6e9b71ce4f723f23aa45ba855e344f9f472e052d199a470b05177b5b2f0b`  
		Last Modified: Sat, 04 Oct 2025 14:50:11 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04ecb4640939c877419c134a32e2ccd424a2a01a8bf71366d72796b48c04c64`  
		Last Modified: Sat, 04 Oct 2025 14:50:11 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:37fd8fee5dc57314d2591c288c85007ea2d51b89c341effb167fd47f0c31ff72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7473759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b27bb8b3e202a3fe19606bfae6d242a3cb747aabaf5563bd1f40b0f41b1a35`

```dockerfile
```

-	Layers:
	-	`sha256:22eabfe225902b96260a095a608ea362e4dbdc774c43990d34252ca59cdeac4d`  
		Last Modified: Sat, 04 Oct 2025 15:37:45 GMT  
		Size: 7.5 MB (7457914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c794887b689e00cf706a8989aef99f9439a843dc05b9c805a8a66a906d76ed78`  
		Last Modified: Sat, 04 Oct 2025 15:37:46 GMT  
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
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
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
