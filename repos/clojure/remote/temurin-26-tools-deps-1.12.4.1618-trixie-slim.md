## `clojure:temurin-26-tools-deps-1.12.4.1618-trixie-slim`

```console
$ docker pull clojure@sha256:387a6b74c9874e747a6fa959731061a59bb98d3fbfc6ef4fa1e56640bbcb37c1
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

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:080d7c710c056a2710408fd6596491b88c16aa3b7d090495d662f454660121c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199210112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7009313039c05b875e62ed339439c41db141825d4f30cb6acd92ee9c7a58b3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 23:37:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:37:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:37:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:37:27 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 09 Apr 2026 23:37:27 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:37:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 09 Apr 2026 23:37:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 09 Apr 2026 23:37:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:37:42 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:37:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ee3f2cd1841f34a437c48ed04b58e918164909f475add21bac50c8c8768e28`  
		Last Modified: Thu, 09 Apr 2026 23:38:02 GMT  
		Size: 94.5 MB (94455682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c28dcafb960b4ad6c307841c335b29d7549ae989477d14723045efb1172860`  
		Last Modified: Thu, 09 Apr 2026 23:38:02 GMT  
		Size: 75.0 MB (74977747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba004ca088687352f3ae2340babd2637a45802ec10f727306658bc32f6887b12`  
		Last Modified: Thu, 09 Apr 2026 23:37:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfae2ad5dbaf275e600dd5f0e022ae30a2fa180f87c183f25364a4edba575cd9`  
		Last Modified: Thu, 09 Apr 2026 23:37:58 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8c72f32e64d8dbdadda7f6be0ced59a68c4a4ce8b797707fbc6f999cacf15ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5240447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc76c64d3e1aca8137b0582c937e4456aca4a7519726087507a4f0324e8073c6`

```dockerfile
```

-	Layers:
	-	`sha256:d6a3af34a05cc67be31ee6766d4c0a48b39449066fe4763ba7d0fa54f845d4fb`  
		Last Modified: Thu, 09 Apr 2026 23:37:58 GMT  
		Size: 5.2 MB (5224642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77b1977634d3bb4bca6111352a000da096685155f44633fdb926ff6425aee17b`  
		Last Modified: Thu, 09 Apr 2026 23:37:58 GMT  
		Size: 15.8 KB (15805 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8521010c4166a2023ab8ed55dc093710130ea8a22974f9734f1568b1f9f8dc22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 MB (198685518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b4056c7392ad0dfcef0e0b681d442f02df0a594307ad939c27396d95dbe662e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 23:37:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:37:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:37:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:37:13 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 09 Apr 2026 23:37:13 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:37:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 09 Apr 2026 23:37:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 09 Apr 2026 23:37:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:37:31 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:37:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e2eab9b30add0e4eb8f7ad55086049c230ee9523ca1004549ab45f74624b96`  
		Last Modified: Thu, 09 Apr 2026 23:37:51 GMT  
		Size: 93.4 MB (93395199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303ed355d086186012c244022e009107cb5584c6c6e03bd203dbc443f41e0ceb`  
		Last Modified: Thu, 09 Apr 2026 23:37:51 GMT  
		Size: 75.2 MB (75150728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f1d0dc34337d18bd3482dc469cb7f840f0ee90e99f4c074eb3d78966f968af`  
		Last Modified: Thu, 09 Apr 2026 23:37:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf10238d139b93d92ceab1eab5accedd7eabb800b7e853e9c693e88bccaf9f4`  
		Last Modified: Thu, 09 Apr 2026 23:37:48 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e71eb2ce69f0a47fc8149fd6912e1543d80640e5dec79ac84b5dab4016912359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5246331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7bae774f49af913abc1c0645ca9bfb7f1b7dd051c5b76b8abb2f908c872c975`

```dockerfile
```

-	Layers:
	-	`sha256:6bc48a1a838f804c86c4a64cc10c3fbe0ccd986cd79a02e0f01349ff2e44e930`  
		Last Modified: Thu, 09 Apr 2026 23:37:48 GMT  
		Size: 5.2 MB (5230408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:245cd888e02b6ade9ea4659017ac48660b1ca0edfeda506214881f62d50ff3e0`  
		Last Modified: Thu, 09 Apr 2026 23:37:48 GMT  
		Size: 15.9 KB (15923 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:a5e0746b08068dffdcfe64ab73d4c09e53b04be72bafe6b06d1ae763c24f33df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.0 MB (207985989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b869cae6c8fbc7787bf00ffe434fb64c444572a3821b515826541cb5c8642251`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Fri, 10 Apr 2026 00:53:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 10 Apr 2026 00:53:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 10 Apr 2026 00:53:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 10 Apr 2026 00:53:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Fri, 10 Apr 2026 00:53:45 GMT
WORKDIR /tmp
# Fri, 10 Apr 2026 00:58:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 10 Apr 2026 00:58:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 10 Apr 2026 00:58:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 10 Apr 2026 00:58:42 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 10 Apr 2026 00:58:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ad9d78de109af0508c6cea77373f8cb08369c373cf24c72f7da9935301139a`  
		Last Modified: Fri, 10 Apr 2026 00:55:00 GMT  
		Size: 93.8 MB (93781481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac72e545ef7eefd4903d47a4d9541b09a6a095df7fdd043f838ec6ab97bea3c`  
		Last Modified: Fri, 10 Apr 2026 00:59:18 GMT  
		Size: 80.6 MB (80610448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5770d7433e19a249b7ef4a5e0d8e1e91476ea5cc03899e54182e4fd200998295`  
		Last Modified: Fri, 10 Apr 2026 00:59:16 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af421ae655820796b85429674b1042a4fbc995ca03e4412b7cc1690a2ce97157`  
		Last Modified: Fri, 10 Apr 2026 00:59:16 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b0a310e5191c13ac2e32c6b853e725e489d445845854c3d1c713dd8453292180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1458c390c765ed0c56bfd94e06fc8c40d5a0c6db200e693b7004e9946591125`

```dockerfile
```

-	Layers:
	-	`sha256:5a709b641737a56a6274ecb32eee67c3d72b9a95abbd68dd2f94d8c45274e3d9`  
		Last Modified: Fri, 10 Apr 2026 00:59:16 GMT  
		Size: 5.2 MB (5212949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32142ab56f0fc414cf6eef6d8fb0a63e2c6f56097fbcf3f42ef0d38f9be12c83`  
		Last Modified: Fri, 10 Apr 2026 00:59:16 GMT  
		Size: 15.9 KB (15853 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:6fb24796d4090956e75d654ea5f27811a14239f71ba679522311f75f1d9cc529
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.8 MB (194804073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419bd355fe4e00310d8e7114e0a873ef92cab9bb60444123006a93a5b333f2c8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sun, 12 Apr 2026 18:55:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sun, 12 Apr 2026 18:55:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sun, 12 Apr 2026 18:55:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 12 Apr 2026 18:55:33 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Sun, 12 Apr 2026 18:55:33 GMT
WORKDIR /tmp
# Sun, 12 Apr 2026 19:18:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sun, 12 Apr 2026 19:18:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sun, 12 Apr 2026 19:18:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 12 Apr 2026 19:18:55 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 12 Apr 2026 19:18:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7fc246f5e32984af9b4236c90104244f3679fa7192854d7e61221c59edbfc2c`  
		Last Modified: Sun, 12 Apr 2026 19:01:08 GMT  
		Size: 93.0 MB (93008131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4ae2605017aa1d6f33c7da5e31a3615d336382b884d351cc650ccabf1abee5`  
		Last Modified: Sun, 12 Apr 2026 19:22:30 GMT  
		Size: 73.5 MB (73519116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4553c37da03beb28ea8bf6c8ec57d0d2a20024234ab8f09c60479ba3643879`  
		Last Modified: Sun, 12 Apr 2026 19:22:19 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feed629c6b5064cb5863f27fa11ebdff40b2166b35c22e22190955ffeb8e264b`  
		Last Modified: Sun, 12 Apr 2026 19:22:19 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e7836bb7109a47dfe5b1959858b682458b389e1a11ea0ee26c3341909e7e34f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15972e24e11f37ed3f438143d5c6c8eb41764ea9cd813215b2d9cbc24bb3d110`

```dockerfile
```

-	Layers:
	-	`sha256:df6b1e3bf94b213db10b32f45bfd62342ae93378c1225c8fa710d1a2a381f63c`  
		Last Modified: Sun, 12 Apr 2026 19:22:20 GMT  
		Size: 5.2 MB (5196741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0e9a89a1e78e2424eb9dd27af47d667fc8b7c0ce5f92bf5e1385b1d6169dcb7`  
		Last Modified: Sun, 12 Apr 2026 19:22:19 GMT  
		Size: 15.8 KB (15848 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:01f17267665ccbfd9a36f8142c24639e7709a529b9f6536eb23d5b8e966fdfdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 MB (195982812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3baa13c2b0cae6abb8ee2856aa8d44efe11b88aec9813a4228320f5b0cb834dc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 23:44:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:44:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:44:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:44:22 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 09 Apr 2026 23:44:22 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:45:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 09 Apr 2026 23:45:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 09 Apr 2026 23:45:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:45:45 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:45:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:82e48a38ec87473a03164a244b5d8dfc2b55ef7a891305e41ee39d937de3c4a4`  
		Last Modified: Tue, 07 Apr 2026 00:13:47 GMT  
		Size: 29.8 MB (29835418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d497ec2816b8b56226d37338bd198a7a45726696a0423458803d8542ce4164ec`  
		Last Modified: Thu, 09 Apr 2026 23:45:05 GMT  
		Size: 90.5 MB (90547693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17966dfe71209fa5e56ca178a8640a7c4b5faf2679380d9f4327586fdd5cfb81`  
		Last Modified: Thu, 09 Apr 2026 23:46:11 GMT  
		Size: 75.6 MB (75598659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1da41daa787455149814a87731e7f31458277c81a65ef7783d6fd98dbcc8e6`  
		Last Modified: Thu, 09 Apr 2026 23:46:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a7eaacae35382805157c284ffc6d8fc6f64e9b7e09bbe4b1dca0b6eb4994d0`  
		Last Modified: Thu, 09 Apr 2026 23:46:10 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.4.1618-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cddd81d5be965ba80167fa33b271387bbfc3580061973f92c166c2f3e77476e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4ad23f0a092c363d747b8718e1ff097f51eb8cd91ca729602f94ff5bb5fe4f`

```dockerfile
```

-	Layers:
	-	`sha256:406f65a6a9c7b500adcfb7c551cbeb6280ed7b837ef15f4591475ded5d97ec8e`  
		Last Modified: Thu, 09 Apr 2026 23:46:10 GMT  
		Size: 5.2 MB (5205752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec20be40b0cdc3260c89c85c6ce9236dec946432692e7e823212c0e6384aa782`  
		Last Modified: Thu, 09 Apr 2026 23:46:10 GMT  
		Size: 15.8 KB (15804 bytes)  
		MIME: application/vnd.in-toto+json
