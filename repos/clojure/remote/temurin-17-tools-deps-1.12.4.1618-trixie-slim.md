## `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim`

```console
$ docker pull clojure@sha256:e7afaf89d9f0b3dbed27aaf00b26959b5197d496c4f62fc7b932856220b7e986
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

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:fd1765f86b3f0fcc132c46da5e39e01c35369366de64063a5e306d79c7265a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247417758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b04987129d58f4bd4bcffd20b24ccbe523790b18f4282cc826c1f742e08695a5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:15:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:15:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:15:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:15:17 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:15:17 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:15:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:15:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:15:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:15:34 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:15:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aeef9b4976150725400f3d51be01fc056c7fee8d4ef1bacd5eb0f9eb5408e03`  
		Last Modified: Tue, 07 Apr 2026 03:15:57 GMT  
		Size: 145.6 MB (145628717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35683e5beea8bdc14423e19a8cb3f605da241c3636568a39694003a69ed3490d`  
		Last Modified: Tue, 07 Apr 2026 03:15:55 GMT  
		Size: 72.0 MB (72012359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef15c25a074e5dbd5c0d7739309524b321c12e5d435db6da436a3f4411bd24e`  
		Last Modified: Tue, 07 Apr 2026 03:15:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16ac7dd7b730c88cc4772aea3a523c5835c40d8e7acc86792547a1dcb64e020`  
		Last Modified: Tue, 07 Apr 2026 03:15:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b3b803b4a7ef41a48a1900643b444592bf67476232c6d3bc4818942c0a4db43f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5274950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7380b86ca57742c03df872472c528e8d55c00f516b5d99c4e4a84ac22be7fa6a`

```dockerfile
```

-	Layers:
	-	`sha256:883d5ece7f86ecae345f110499424cc490ef9cc9f55231d31f8d16285f6807fb`  
		Last Modified: Tue, 07 Apr 2026 03:15:52 GMT  
		Size: 5.3 MB (5259138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eceeee01478007043013d960a719757983b4c9aca31470d8062ab463cc67a1b0`  
		Last Modified: Tue, 07 Apr 2026 03:15:52 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:77a07a395333d0e5525f9f88e285cb35ff955de7b64cfaabe4aa9036a53b962f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.4 MB (246407328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d6e17d30776104d08e36181a8f30615032702cdfb464c83c6072b05edd627b7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 03:25:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 03:25:58 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 03:25:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 03:25:58 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 03:25:58 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 03:26:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 03:26:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 03:26:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 03:26:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 03:26:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d6c4fc109c3b8daa3acd20f621fc415c4da4df34b15e2c82dffe5f3d189c2f`  
		Last Modified: Tue, 07 Apr 2026 03:26:37 GMT  
		Size: 144.4 MB (144436221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42225e6f6fe7629b218f3382402c64c2df29c8943aeb70c784952a365098483`  
		Last Modified: Tue, 07 Apr 2026 03:26:40 GMT  
		Size: 71.8 MB (71831512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353767225f21eed1ba6d62ea8f350f2cac767f020bc0fef7b8b5bfc7fa536326`  
		Last Modified: Tue, 07 Apr 2026 03:26:37 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab43ec63bd43620e926673639bbd014f7273b46eaf37731316a40c1aff5f7f01`  
		Last Modified: Tue, 07 Apr 2026 03:26:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bcca091965065dd21b7194f8be887e15aaeb34d44c141b45327d4176cb2b3359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5280837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d50032ab2e58d9773e01b37ec3ee0bbe6735ed662ddd803ea39136072a63711`

```dockerfile
```

-	Layers:
	-	`sha256:6d287603c9d4c9068ded3875adbab300a0a0220a6e0bea02ea5ace2c042e854b`  
		Last Modified: Tue, 07 Apr 2026 03:26:37 GMT  
		Size: 5.3 MB (5264907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b709f4fae219884e8804e8c3d3a287b0c406aaf573a74f697e849d942302e482`  
		Last Modified: Tue, 07 Apr 2026 03:26:37 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:c932626533105e9693472996ce23af98f761cedceaa249fa90047d7ccf658840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.5 MB (256462008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453102d3672d3808fdde84e494af15f8ecb7ce3382862927ab9109c702bc1b7f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 14:40:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 14:40:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 14:40:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 14:40:02 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 14:40:03 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 14:45:01 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 14:45:02 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 14:45:02 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 14:45:02 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 14:45:02 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3932a79f80dcbdd923f767310a5e86b8d32b8b0ffe1fd3bdd6bfa835cbf4e1d1`  
		Last Modified: Tue, 07 Apr 2026 14:41:24 GMT  
		Size: 145.4 MB (145438259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7997d6550362fdc22a1c84152a6b3c4e7a7558e7e2d8d6b43cafddc805c5baca`  
		Last Modified: Tue, 07 Apr 2026 14:45:41 GMT  
		Size: 77.4 MB (77429693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a363f4f60082d7684955baefbeb75b9ecec101e6f8541ff2c222861b802c1c`  
		Last Modified: Tue, 07 Apr 2026 14:45:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59afa82229598f9eddba177a92ea290f76e96b8a1625705da54a619fcbd8b8a3`  
		Last Modified: Tue, 07 Apr 2026 14:45:39 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:023ab5b3fe0e55e19aaf8599ec8157a0e6a39863bd1f289208ab441b94549a72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5279369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cd7d7f8ee149c23374687250b85bf680d5f06fbd79f49e31309a09dcceeb3b1`

```dockerfile
```

-	Layers:
	-	`sha256:70f401a31c89821dc131dc8b9db8510dda02c13140d2d7df030acd704a05baa3`  
		Last Modified: Tue, 07 Apr 2026 14:45:39 GMT  
		Size: 5.3 MB (5263509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2c127b670a94433e5a0360b555069fe333f0eb5a09236104374f88aa4e15339`  
		Last Modified: Tue, 07 Apr 2026 14:45:38 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:00e01b4a07c0985bc4b891d6f3febed253dac5b2ce7211836fe0faf33ab1b985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.8 MB (241840408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d2d414b5285e495cb80b8a8afd735d5da67ad352ce4a9858a8f221905647517`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Sun, 22 Mar 2026 18:36:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 22 Mar 2026 18:36:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sun, 22 Mar 2026 18:36:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 22 Mar 2026 18:36:25 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sun, 22 Mar 2026 18:36:25 GMT
WORKDIR /tmp
# Sun, 22 Mar 2026 18:39:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sun, 22 Mar 2026 18:39:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sun, 22 Mar 2026 18:39:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 22 Mar 2026 18:39:05 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 22 Mar 2026 18:39:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0b5164900a4737bd8c71921f9d6095f2a9499d5081755c56a4aa46d8f37e9865`  
		Last Modified: Mon, 16 Mar 2026 22:10:41 GMT  
		Size: 28.3 MB (28275636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc59ab8223d6223d60aa7ae5a907145f2fb35e6994bbb8454d7fb04c39041b0`  
		Last Modified: Sun, 22 Mar 2026 18:44:02 GMT  
		Size: 142.7 MB (142662945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98deadc22b1c1212b4fb6de09789a809c36f59f9b411de2c8c810541cbf48302`  
		Last Modified: Sun, 22 Mar 2026 18:43:51 GMT  
		Size: 70.9 MB (70900783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9fc2e77cea1f6c3aa9658a5a7ecdb1f8a19d0b21f5266d61e1b0f1e42ada3d4`  
		Last Modified: Sun, 22 Mar 2026 18:43:31 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bd868365bffd3ddc84ffb5c9bb3f000252a7578c38ca1b78cdabbbfde52203`  
		Last Modified: Sun, 22 Mar 2026 18:43:31 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:61d4fd6c45e3cb432091152228f3a68d2b444d92b0b19c85e861dacacbd12f0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5262543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8bfb7aa7f297ca68ec8b24cd4ed08ea0a3dcce50dfeb437b47705e27d502307`

```dockerfile
```

-	Layers:
	-	`sha256:7d333bbe1fee8cf85a44db1f486a65f290e96e911f3b9c986abc3d7a3c32a9bd`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 5.2 MB (5246683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98fab935bf965abbae051ca66d10af18beeae154cf74bca7d8f230024c7e7e2c`  
		Last Modified: Sun, 22 Mar 2026 18:43:31 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:d069f9338cc76a8e005380aa14233a9ea0e376f3fa29a9002f97d67b4c26580e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.5 MB (238450392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7552201f934ab07cde83409a1ee736243bf412d95f62ad3ce1ad514a6631e8dd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 05:43:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 07 Apr 2026 05:43:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 07 Apr 2026 05:43:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 05:43:50 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 07 Apr 2026 05:43:50 GMT
WORKDIR /tmp
# Tue, 07 Apr 2026 05:44:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 07 Apr 2026 05:44:06 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 07 Apr 2026 05:44:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 07 Apr 2026 05:44:06 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 07 Apr 2026 05:44:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09a62589dc61ae10c60d17a1a4f5af8f6163dc02e98bd93e0c3b8d53da1eb022`  
		Last Modified: Tue, 07 Apr 2026 05:44:35 GMT  
		Size: 135.6 MB (135626852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb564360cc4f6dc90e79e1b786ad9f47f5c3cf3f6388b1e1ecc16214d3e19e3`  
		Last Modified: Tue, 07 Apr 2026 05:44:33 GMT  
		Size: 73.0 MB (72987080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8b541a77ea5c27f69c656d36c89c92f70ef013005e0ac21e4db93974e9fef4`  
		Last Modified: Tue, 07 Apr 2026 05:44:32 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc53d8de446b44b0279227c20f70be383644e5c69bcecf92b429d4979d6e9cb4`  
		Last Modified: Tue, 07 Apr 2026 05:44:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c5cf4e6795f1a8629383264824a3129623af5b6a2097235bff3e32276b7aec49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5270874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbea0b9aeac49e37c9f2f089a7ee113b96c112cb7a036e93afa05d681ea9422d`

```dockerfile
```

-	Layers:
	-	`sha256:25b2e32c366abe86eef7b7aa90eabc8a964e1cdaf1f3e11a5cb12a97ffe73ef3`  
		Last Modified: Tue, 07 Apr 2026 05:44:32 GMT  
		Size: 5.3 MB (5255062 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71e05d8225608aa9b7d24ff321e643b72a474d09d20bd73f48b3bf3e5223fd24`  
		Last Modified: Tue, 07 Apr 2026 05:44:31 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
