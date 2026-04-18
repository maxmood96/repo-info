## `clojure:temurin-21-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:4dcf84ec8b82ad0427a8b89d9e229ccde3377bd5bb72358563f5384f6938d949
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
$ docker pull clojure@sha256:00031ca44f34fe71c5ba80966fe9ee437eff5e1c17993111574439f1459c4999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262611184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f114186e1fe4015a8740cafc78dbd0ae63d82ad98a5cc7f193a99f3d63a78a6b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:05:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:05:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:05:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:05:53 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:05:53 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:06:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:06:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:06:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:06:10 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:06:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2885dac90438a509e29959d4bd33fb5fe6fee467e6c62fbeeddabbcde52bb336`  
		Last Modified: Wed, 15 Apr 2026 22:06:33 GMT  
		Size: 157.9 MB (157857104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92382b862c58f85c8d32f56949c2d5da5de6738562378482dca0c338d1a4d273`  
		Last Modified: Wed, 15 Apr 2026 22:06:32 GMT  
		Size: 75.0 MB (74977397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4860450cc110e276716db01094f1e1b08fedbfa2612204fb52c079012021e343`  
		Last Modified: Wed, 15 Apr 2026 22:06:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47aa80ff125510393032d10241b1fa13736e0cda6c085c273aebdfae0e50463`  
		Last Modified: Wed, 15 Apr 2026 22:06:29 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d9ce660652e122529541f5137e41a6adb83d621fdc2609f534f600d5327b9027
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c8c5abf01d2eb4e988e105bcbf4f248703f9a6886cebe8ebf751c1249d17df`

```dockerfile
```

-	Layers:
	-	`sha256:df7f56342014ccf5014ffb5c2fb9c2e1fd0d8b30c64421d0a70489ea01d70157`  
		Last Modified: Wed, 15 Apr 2026 22:06:29 GMT  
		Size: 5.3 MB (5260990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f896d50f6cb1e3d0d1a00850cc2eadf9eb98313de8eab707a5390f239db1809`  
		Last Modified: Wed, 15 Apr 2026 22:06:29 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aebb39eb711f2438dcacb0e3f56d7342bcbee023890f0571ea5a6f3068fb9c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261422201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067cce409dbd26662519946a01181ff186af2550eecb786c220959feb117c48b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 21:52:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 21:52:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 21:52:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 21:52:39 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:17:23 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:17:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:17:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:17:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:17:43 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:17:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42232e8bb27cea0b0aaf7557129f3c3442ac8c57671a365e103e8938ec715aee`  
		Last Modified: Wed, 15 Apr 2026 21:53:50 GMT  
		Size: 156.1 MB (156133044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00786ba932eca9349d3cdc66bfe193703734f01a8d430836ba44f14b63602094`  
		Last Modified: Wed, 15 Apr 2026 22:18:04 GMT  
		Size: 75.1 MB (75149570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b98f7e53346359dc3652e532d0420c35239f33d60b3003d4da6bfd3669aa1147`  
		Last Modified: Wed, 15 Apr 2026 22:18:02 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8d5e1731edc1677b62c5b8d93c3d2f8d660b525004a5a6593222561e7bdf5e`  
		Last Modified: Wed, 15 Apr 2026 22:18:02 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:583b4bd15f6e32d772463a51d541c8d56cfaf41f62e54fb4914d23197652bd91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64204ac513ad4ee117090a97ee717aa53dea5682c68e539523feae77b44b156`

```dockerfile
```

-	Layers:
	-	`sha256:7d67e57719de0ffb42342ada719be0bbd78eb0b221a4de9dcd9bca351d6df8d2`  
		Last Modified: Wed, 15 Apr 2026 22:18:02 GMT  
		Size: 5.3 MB (5266759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a379fe004afc28738312184177a9aea7958b5efec847972023af123f5953f30b`  
		Last Modified: Wed, 15 Apr 2026 22:18:02 GMT  
		Size: 15.1 KB (15129 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:954b6c79db8971a394446f419274abbd0bd43a8ee2501537b505316e037e7a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.2 MB (272181831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:648a5c19f6c3edb7ba28ffca9598335cb70523c8e35b52035ee1b7dc21700d05`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 03:01:40 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 03:01:40 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 03:01:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 03:01:40 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 03:01:40 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 03:07:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 03:07:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 03:07:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 03:07:33 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 03:07:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6266996408f18fa5b8afefdb178402a7bc9517ccfdc1fdefe8e27ee9d954dade`  
		Last Modified: Thu, 16 Apr 2026 03:03:20 GMT  
		Size: 158.0 MB (157977492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0712d593bb6889f8e865a5a3a81735a6b0b3ec22fead7c52236f76cdadcc1af`  
		Last Modified: Thu, 16 Apr 2026 03:08:13 GMT  
		Size: 80.6 MB (80610282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef32de035f25055c3f14c2fb2855e55630004c7edbb443c1a8389e33260da5ab`  
		Last Modified: Thu, 16 Apr 2026 03:08:11 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cc34b85539e026ded921876144b7c9d83917b58b4d56cb2c22accf915ad068`  
		Last Modified: Thu, 16 Apr 2026 03:08:11 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:83cb8a7cd1a34b463e7ff424082d8b3cd9fe19ec0f524eeda1a6e2c52c72b644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa49fed52e658207712d28330206baceace9e70f96b6c6ce59dcef044d2114e`

```dockerfile
```

-	Layers:
	-	`sha256:3736b4a7efdeba30b0eaa9b04c8493f0bdea5162d0666c47b4a2b62ca0d1085e`  
		Last Modified: Thu, 16 Apr 2026 03:08:12 GMT  
		Size: 5.3 MB (5265361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93c754517d3dc2d8e3b0e608dfb085d8a5f4b6b27e4f382727a5dde87356d98f`  
		Last Modified: Thu, 16 Apr 2026 03:08:11 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:9aaa235811d943460147dff0fddc9a3a60f4413851950d721debbf98740130b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.0 MB (259012426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c85c05788176c5b267ca86c4987f8fd4c7e679966091aabea86ea8ea61d919`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 11 Apr 2026 22:00:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 11 Apr 2026 22:00:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 11 Apr 2026 22:00:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Apr 2026 22:00:57 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sat, 18 Apr 2026 04:49:20 GMT
WORKDIR /tmp
# Sat, 18 Apr 2026 05:11:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 18 Apr 2026 05:11:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 18 Apr 2026 05:11:38 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 18 Apr 2026 05:11:38 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 18 Apr 2026 05:11:38 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5427f8f7357cd1c2f90f35451416b331ea3c682f95a93bd8689b142ddc99805`  
		Last Modified: Sat, 11 Apr 2026 22:07:07 GMT  
		Size: 157.2 MB (157216895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd9e65888bdd1763a340eae3ac6cae1421f830ecdd9a6291a969293a322dc1f`  
		Last Modified: Sat, 18 Apr 2026 05:15:29 GMT  
		Size: 73.5 MB (73518706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f097ec60300d12b67429b5cf2d0d9b3ab4c27f3c70b6d4905b444d708f82f9d`  
		Last Modified: Sat, 18 Apr 2026 05:15:16 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a77067a97433f03846e8e0196bddc16e5c6cdc6f86a336732438ca3ace731dc`  
		Last Modified: Sat, 18 Apr 2026 05:15:16 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fcedf84ffd77afb380968c9aa27b977b93e5b1a013dc1275bb55d428fc147036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5266314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83713c3c625ede87fd84c21ebd9bb6bc8af295a1337bc9a80e97aafeec7b4b73`

```dockerfile
```

-	Layers:
	-	`sha256:abdafee2cf231bbed3b9ef8bc59479903e8f8e5406cfb02e0f0e12e95e57f1c6`  
		Last Modified: Sat, 18 Apr 2026 05:15:17 GMT  
		Size: 5.3 MB (5250454 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:059614943fe787b967406e7b1c24bfd6f7df571922b7c29932a26b474d0dd622`  
		Last Modified: Sat, 18 Apr 2026 05:15:16 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:52ba36cc5236fcfbe8df82c2ae03d5d5fda78a802416f3957622ba9738608021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252540260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:723ddd7f0c592425a484cf00a1a608cef767ff723d8928cc4061274752cb3f9c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 00:41:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 00:41:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 00:41:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 00:41:51 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 00:41:51 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 00:43:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 00:43:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 00:43:19 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 16 Apr 2026 00:43:19 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 16 Apr 2026 00:43:19 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcda4ee8bd621aac2ef8027b80495558658cc850eca58d63e93743bca8b01b4`  
		Last Modified: Thu, 16 Apr 2026 00:42:33 GMT  
		Size: 147.1 MB (147105251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07e97b5ac60e80fa6914b0b0d53fa4d2e8eea4eebac818afe7e383010306e40`  
		Last Modified: Thu, 16 Apr 2026 00:43:43 GMT  
		Size: 75.6 MB (75598549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a928ecfbb6d351d813a5b226036f14229d0424ead99ebb83a83070aa404b55`  
		Last Modified: Thu, 16 Apr 2026 00:43:41 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57078e2cab2d2894567179d961edacc2fbdbaeb24095cb2b7cffaeb1d3094b83`  
		Last Modified: Thu, 16 Apr 2026 00:43:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:01cb671e4d7870de262c0cd35347cd0c8629c08dc927b50ddf922267d6899d6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c5f393c75511586cc925b84a3e1785a8d673fd6f3b33ea0041d8c2c8ebc77f`

```dockerfile
```

-	Layers:
	-	`sha256:122844a4fa6911d9e102a96e4216bc8b4fea900dab43859a2b660a836654ea13`  
		Last Modified: Thu, 16 Apr 2026 00:43:41 GMT  
		Size: 5.3 MB (5256914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cd3fec23fafb919d2372e0ecb10e9f2efeb1563d9f7c386742b46d7354bbca2`  
		Last Modified: Thu, 16 Apr 2026 00:43:41 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
