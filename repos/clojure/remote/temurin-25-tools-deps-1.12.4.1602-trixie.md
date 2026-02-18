## `clojure:temurin-25-tools-deps-1.12.4.1602-trixie`

```console
$ docker pull clojure@sha256:adbffa0a484d021749b8f9c54e6671c9dc5acbcf4c610c653531587e070e3249
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

### `clojure:temurin-25-tools-deps-1.12.4.1602-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:de20ccfd09fd294ceb6db1bbc4b265b289c92172d913f1f0ebe7f69346620e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 MB (227092768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97de95120418d06966c0c01253da9a4cd772875ff6f37f75a8399dadb75b62e3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:46:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:46:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:46:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:46:04 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:46:04 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:46:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:46:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:46:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:46:22 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:46:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68df36d26436164302b4b7f6da050afa7ebe8834b3d45d768caa38a3c60542b6`  
		Last Modified: Tue, 17 Feb 2026 21:46:47 GMT  
		Size: 92.3 MB (92256289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19cf9dc47ebdf078ad6dff90e2163cbac52606428e682d451bc5d7323ab59b4`  
		Last Modified: Tue, 17 Feb 2026 21:46:46 GMT  
		Size: 85.5 MB (85542484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2afeb715b2685253c0810829f6f9b47e29dd909e9f0bf4c3a98e32c56dbf88`  
		Last Modified: Tue, 17 Feb 2026 21:46:43 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06974e2596c8486691c15188f7cb63d4759e27e52c6df51e01ba43792ee49ccd`  
		Last Modified: Tue, 17 Feb 2026 21:46:43 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a00a17690eba24420b3ec95f124cb92f408a0e212a7525583b8c91af2869e375
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7453561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b4f8024435830250db71f4ecf9b9e7de3f2a08c48e504a562961e5f1977031`

```dockerfile
```

-	Layers:
	-	`sha256:1c35e4c3f426a2212c204ead13444e9ea93dfd27e34430a4d86a554bdc21202a`  
		Last Modified: Tue, 17 Feb 2026 21:46:43 GMT  
		Size: 7.4 MB (7437146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a389276632ba237d867a23ad3cff8a1614f76eff07efe9b59d1e2b871d1d21a3`  
		Last Modified: Tue, 17 Feb 2026 21:46:43 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1602-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3a1a8e4257404e02cd48041d20a68f3e8ef4d2f0827d0ac59da05c7132ee5a45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226302914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb7383fb71e4e76f353ac9d824d1c17f4bdefc4cd2674be4e36a06ad3f34f4f9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 21:46:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:46:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:46:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:46:05 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:46:05 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:46:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:46:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:46:25 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 21:46:25 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 21:46:25 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1bd4defc8c5e5cda3d1685bbe52bfcd79e4448ee97883913300e5d29ca8fdb89`  
		Last Modified: Tue, 03 Feb 2026 01:15:56 GMT  
		Size: 49.7 MB (49652017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939c24eab62892b5595f8e825217ff1661468c15d629eb1bd8fc974cab50e097`  
		Last Modified: Tue, 17 Feb 2026 21:46:48 GMT  
		Size: 91.3 MB (91288273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa8bef98f33baeb1d9f42b44f7f8671e2f9e92269856339ec6b2f4fb2c133da5`  
		Last Modified: Tue, 17 Feb 2026 21:46:48 GMT  
		Size: 85.4 MB (85361580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260e7fd5bab64ec56dbec4048f4445178f03198428961a3f211356ec42eae521`  
		Last Modified: Tue, 17 Feb 2026 21:46:44 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c001ec5c735fd04826246b97ca518c4f67bb332ffb952184468bac33f1e761b2`  
		Last Modified: Tue, 17 Feb 2026 21:46:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cbe29a65e1412ffa735f7034c556cb712b50164b0da4643a910a1b96a3c83074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7460754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3700edcc8a7d446f3b00ebd39faad3fe9f9a4903f6dbb7fdd726b45b403f455b`

```dockerfile
```

-	Layers:
	-	`sha256:65b518478384b60ee32238e0776065a9a8399f4201e985e7a0f21731f55a2bac`  
		Last Modified: Tue, 17 Feb 2026 21:46:44 GMT  
		Size: 7.4 MB (7444197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:373bab926f21423517559a1515e9147fef44c08725efed8470ed76a578b55ca6`  
		Last Modified: Tue, 17 Feb 2026 21:46:44 GMT  
		Size: 16.6 KB (16557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1602-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:5643c402346eda3e9f962de5844b98d9edf67e4a6f3ed65a013ce9fac394d69a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235693564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b319f930a00829982ed3c066c41e674dd1aea7f19a1a5421f9771ed5da2318cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:48:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Feb 2026 00:48:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Feb 2026 00:48:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Feb 2026 00:48:05 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Fri, 06 Feb 2026 00:48:08 GMT
WORKDIR /tmp
# Fri, 06 Feb 2026 00:53:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Feb 2026 00:53:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Feb 2026 00:53:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Feb 2026 00:53:29 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Feb 2026 00:53:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6397fc946e64e7714633f42a4de42b00c617e66212cd1a0b61df76767b81f868`  
		Last Modified: Tue, 03 Feb 2026 01:16:36 GMT  
		Size: 53.1 MB (53112115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3230ebb877a1444adbcad5521afaffb1c41773004c4324fe65c2c551a9cc1544`  
		Last Modified: Fri, 06 Feb 2026 00:50:07 GMT  
		Size: 91.6 MB (91632873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ef605411196c730ec201e18c625f2cabfc5fb83efd9aa74fadd830038fa9a6`  
		Last Modified: Fri, 06 Feb 2026 00:54:13 GMT  
		Size: 90.9 MB (90947534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f44e46ba657109043e4bd78d3e9efe1f54b96ba06b92d73b3b462d3a1921ef8`  
		Last Modified: Fri, 06 Feb 2026 00:54:10 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655167cc00123f09c2a88756e426950971b5bfb6f02d958b0054e20f8bdf753f`  
		Last Modified: Fri, 06 Feb 2026 00:54:10 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:78d0f2d5872d09ddcade682857b713cace1babc67d5b4bfd6a2a171194ec139f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2642df4963aac19dbb1d0191df0c6d20de8fe59ba430e1c582f221fd05a9f255`

```dockerfile
```

-	Layers:
	-	`sha256:b651bcedae4c7cc363e070c930a7d225a0b867b1039a5df57fd310e3161dd6f4`  
		Last Modified: Wed, 18 Feb 2026 00:06:39 GMT  
		Size: 7.4 MB (7424891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c5b8fc6137227c3a49466d1615b2a4e1d017c3fe4da9a4b06f267345e97b19f`  
		Last Modified: Wed, 18 Feb 2026 00:06:39 GMT  
		Size: 16.5 KB (16474 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1602-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:d5569ee77cb3ebcf946dee5a7847aff6c8494794b99bf7b61da8e7a70af95ad9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (222976497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ceb23e150cde9679316e50fb4570cecb5568c47a471d5bac776bde32b78895a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Mon, 09 Feb 2026 12:53:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Feb 2026 12:53:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Feb 2026 12:53:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Feb 2026 12:53:52 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Mon, 09 Feb 2026 12:53:52 GMT
WORKDIR /tmp
# Mon, 09 Feb 2026 13:17:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Feb 2026 13:17:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Feb 2026 13:17:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 09 Feb 2026 13:17:05 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Feb 2026 13:17:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:618efd37f74728f7dcba60c231fad7f2d777dc65e4da32d0adae5e032e1fd125`  
		Last Modified: Tue, 03 Feb 2026 07:13:10 GMT  
		Size: 47.8 MB (47776763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b3877762b7849aab190bdd4be4bec0fdbb7a69de6798289c7ab36fcca52b2c`  
		Last Modified: Mon, 09 Feb 2026 12:59:49 GMT  
		Size: 90.8 MB (90773405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7a7bd39b64d0ecb8e2cc915d3c5439746c541601c6300994a66c45379fdcb3`  
		Last Modified: Mon, 09 Feb 2026 13:21:34 GMT  
		Size: 84.4 MB (84425281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9673f630eeaeb35ec8357819cbd1a9dd8ad789789e4529ca630afa2ebac361`  
		Last Modified: Mon, 09 Feb 2026 13:21:20 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085a0895fdda4f397f81a0b372fd0fb6ba827fb6047ee1fd5aebb5aadf429841`  
		Last Modified: Mon, 09 Feb 2026 13:21:19 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6f5eeba02584c02b4ae87e440262e258109157a2f8d652ac931aba174040c5ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7423559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a773f93a951fb71e638fb79235b158d356cc55e99c17628b5965f61ed96227e3`

```dockerfile
```

-	Layers:
	-	`sha256:7b2ba88d4a556718cf507382514a6b77830c14a7a1f7b7582960d7ea5a3c1fb9`  
		Last Modified: Mon, 09 Feb 2026 13:21:22 GMT  
		Size: 7.4 MB (7407084 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba9487606bdf153d91e4c66c11380a1195cdd173e0217de6f09d3568f07dd7ca`  
		Last Modified: Mon, 09 Feb 2026 13:21:19 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.4.1602-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:e8341560379628ad7823aa48a6e0fc84d275837a2f84c4f8b529a6c80f7e4d41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224101332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32413711f764c5e98ee87701c1e73bca4bbd3e071b5766814fe3cca5ac1ba9f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 17 Feb 2026 22:19:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:19:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:19:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:19:35 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 22:19:35 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:20:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 22:20:30 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 22:20:31 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 22:20:31 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 22:20:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5578086c4ad67b3331d31c74c0b8aa3d13821b75ffa03070b0c1c80fdba7ceaa`  
		Last Modified: Tue, 03 Feb 2026 01:14:13 GMT  
		Size: 49.4 MB (49354378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac064884eca297fda6b77725e0502ad7ae6b62db38d8cbd2ad4c4340d2bd416`  
		Last Modified: Tue, 17 Feb 2026 22:21:19 GMT  
		Size: 88.2 MB (88233833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fe20b6831ce4ebc6b102c20849a866163dfbc9a171e78413c0afab26e1c57f`  
		Last Modified: Tue, 17 Feb 2026 22:21:19 GMT  
		Size: 86.5 MB (86512075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55eb9af37e3f6f33676169b03e4a2e528b57ada6c36ae198030489480480c413`  
		Last Modified: Tue, 17 Feb 2026 22:21:17 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8949eefb4c24ec43075a6a607f27114484aaac5a838cc776ff3d210abd986982`  
		Last Modified: Tue, 17 Feb 2026 22:21:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.4.1602-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:30074d6b5a555b57589f45f950f9c5f671474b192845322887eef80b3a93e5bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb691ce07f297cbcda1d026cd394ed0e1d02205e6c429a3d4f4d4d7c33e1f507`

```dockerfile
```

-	Layers:
	-	`sha256:76828d15e1a8b0122213b2997d55425d5cce7adbfd35324b877337bdf41271c4`  
		Last Modified: Tue, 17 Feb 2026 22:21:17 GMT  
		Size: 7.4 MB (7417630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdbdbcaea02a2878157828d7ec5f74e454ecbbe0af022c46ee71cb0f8439e0ad`  
		Last Modified: Tue, 17 Feb 2026 22:21:17 GMT  
		Size: 16.4 KB (16414 bytes)  
		MIME: application/vnd.in-toto+json
