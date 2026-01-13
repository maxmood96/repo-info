## `clojure:temurin-21-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:8bc93db464e18223847d315e4276237c10372c3e6fb5088c98bade007a03066e
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
$ docker pull clojure@sha256:5fb03a5f1dd379a1bb735911dbc363d25693ef01a7cee4242c8c417d04f91276
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.6 MB (259594431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15eacce39c13a33415fce4e3d213d7201c75ac41511fead156df89146fd0fb4f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:37:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:37:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:37:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:37:04 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:37:04 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:37:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:37:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:37:21 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:37:21 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:37:21 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8eca189fc22d090c084835e2ffdc36147acb1f26e11adc785a4b3597ac650d`  
		Last Modified: Tue, 13 Jan 2026 07:46:27 GMT  
		Size: 157.8 MB (157826042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714eece54721fb9e897a0837f33b1cf11053ce9b4dab63eee8271a4fdada628`  
		Last Modified: Tue, 13 Jan 2026 03:37:57 GMT  
		Size: 72.0 MB (71993663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d50b5f1d86398793404bdffc1b1ffa75a80b6744035bad35a633a2f740777c3d`  
		Last Modified: Tue, 13 Jan 2026 03:37:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91065066ae3e72f0c677119f1a647e95eee4ad32bbbe8f3d90bfa9a5c5db8914`  
		Last Modified: Tue, 13 Jan 2026 03:37:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aab6bef2e7310b19f59c74600076ddd1f34a5d9ed750fdd14b5382179f9cfcd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5275211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d836909a3c310990a46b6ae1e32ee4ad82aea4bf98916e0f04d2f44e95a553ed`

```dockerfile
```

-	Layers:
	-	`sha256:f2b9a5bda17fb7248e6184dfe7eef77aec49c868723c78e85bbd2e084ab53543`  
		Last Modified: Tue, 13 Jan 2026 07:44:48 GMT  
		Size: 5.3 MB (5259399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a4d99f58d71e53280e796515bcda25a6c1d0b0e1889db15af63e8da8af66dc8`  
		Last Modified: Tue, 13 Jan 2026 07:44:49 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:29db4742b456bddf512740b1fb140e02e5189295df700bd4b7b01f253d59ad3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (258048906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:329df44aa7f336ad38c7f04c748fac7074253ca440f05900ef4a8237e3625a1b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 03:40:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 03:40:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 03:40:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 03:40:28 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 03:40:28 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 03:40:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 03:40:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 03:40:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 03:40:46 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 03:40:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd47734824cb542b97126bdd129a33b055e918b1c65f2bfe49ff74eb6ae8de6e`  
		Last Modified: Tue, 13 Jan 2026 15:11:44 GMT  
		Size: 156.1 MB (156107580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe61ba5ba6064d2e24e9e8283a9168e3ef917969164e1f168a910a72beb4a3b`  
		Last Modified: Tue, 13 Jan 2026 03:41:23 GMT  
		Size: 71.8 MB (71806242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9a9617a37e21518daa0d3a0699b9435e32e98903ed27b0c593402986855557`  
		Last Modified: Tue, 13 Jan 2026 03:41:18 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7808acae8c6ea5db73ccb13d88be53494403685013e5fd0408042bbb54b21d`  
		Last Modified: Tue, 13 Jan 2026 03:41:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1a48624c5542be90de3938fc8f1eaefd7a84a433fe8485d968f7eb34e615fd20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5281095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aecc6b2ba2e0bf00aa6008ce82485ce31836a656149e0869a83b506fc78e275`

```dockerfile
```

-	Layers:
	-	`sha256:69fff6a8cfb403381fc47f7629a559350a6889b602b0dceb0e6cfbf4ac27a261`  
		Last Modified: Tue, 13 Jan 2026 07:45:24 GMT  
		Size: 5.3 MB (5265168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af850d9e5e402939f07f217fb0b788f2a830b9f42cc7d53bc96ce93cd30ed66d`  
		Last Modified: Tue, 13 Jan 2026 07:45:24 GMT  
		Size: 15.9 KB (15927 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d1913ab1b15b070bcce4f8216486119b8ca49f9b6acd7690ba9c037ecbf32535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.9 MB (268929702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb96a3cfb80fbe01eb49ca9411e80301a3b2dcfc6f0eca20c49e524907968e8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 05:47:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 Jan 2026 05:47:27 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 Jan 2026 05:47:27 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Jan 2026 05:47:27 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 13 Jan 2026 05:47:28 GMT
WORKDIR /tmp
# Tue, 13 Jan 2026 05:50:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 Jan 2026 05:50:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 Jan 2026 05:50:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 Jan 2026 05:50:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 Jan 2026 05:50:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58a834387b09bddb874696b527c7ae70b8166b6d2486c2a53584c23551b3001`  
		Last Modified: Tue, 13 Jan 2026 05:49:08 GMT  
		Size: 157.9 MB (157942939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c4eb308fadfce98a8a3426ee1c16154dc3033c94c54f19fcc54ee090cf4d27`  
		Last Modified: Tue, 13 Jan 2026 05:51:43 GMT  
		Size: 77.4 MB (77390121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb09efa8f2edc769badf0061b2b2dcc4da7f350d15dd29c383a7d3f69334d8d7`  
		Last Modified: Tue, 13 Jan 2026 05:51:32 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:357ebac76461c8cc2dfaea2cc5c430bf96def477ac15980dcf69460e204143ad`  
		Last Modified: Tue, 13 Jan 2026 05:51:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:485182f2dff8eb951369d7a90655bbc776b1ca8f86fc952520e639b87f2bf043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5278829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e916a3186109b6a42fc4ec0c412067988370a32262c3aa8bdb8c78d3310f105`

```dockerfile
```

-	Layers:
	-	`sha256:ab085e9f8226fc42d70af8f7eeab028f35131ebf4c682164cb593fff9138ccf9`  
		Last Modified: Tue, 13 Jan 2026 07:45:30 GMT  
		Size: 5.3 MB (5263770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1abedc6c52ec4c3211e43c8a64d72c88122731d488814e31a8df483fc49a2c3`  
		Last Modified: Tue, 13 Jan 2026 07:45:31 GMT  
		Size: 15.1 KB (15059 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:67cd579232b51203a3dc13b303cbe8615108f9c08fd30fcce37235fe31f04664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.3 MB (256346826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d6e76c45c6ffb4623aa308d2eb2f7e058c36158f1eed21588323d911d91a44e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Thu, 01 Jan 2026 07:02:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 01 Jan 2026 07:02:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 01 Jan 2026 07:02:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 01 Jan 2026 07:02:49 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 01 Jan 2026 07:02:50 GMT
WORKDIR /tmp
# Thu, 01 Jan 2026 07:19:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 01 Jan 2026 07:19:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 01 Jan 2026 07:19:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 01 Jan 2026 07:19:57 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 01 Jan 2026 07:19:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091162d898a2d4e7b50f7bb9588aeb36e7979c2a93097ad0bdcd2473aa01fb84`  
		Last Modified: Thu, 01 Jan 2026 07:09:19 GMT  
		Size: 157.2 MB (157194291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b596bea77b5945f1b112128096634da44c9318253db5c4a5d2e7e3264007b7`  
		Last Modified: Thu, 01 Jan 2026 07:24:11 GMT  
		Size: 70.9 MB (70878363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6257729749f6b2bdc6b07d335123d519a150a21ec4fdb22e5857cec4645bac16`  
		Last Modified: Thu, 01 Jan 2026 07:24:02 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fd48c429a24d9fcabd2d239fc71b9f43db7daf050603101ce83ad55dbf3acf`  
		Last Modified: Thu, 01 Jan 2026 07:24:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bb4bb828e91d6f09b34605193fdb1084fba497b4221692e904e76af7b9509fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80f7527c92c3b15b147ca02fb0d7ad7ab326bbe6fd2d318503e5585ad07a4bf`

```dockerfile
```

-	Layers:
	-	`sha256:88233960f8e761e594c8af3dbcbea20f0052acb9d6f2b64a3627a9d7ae7bb413`  
		Last Modified: Thu, 01 Jan 2026 10:37:13 GMT  
		Size: 5.2 MB (5248765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4090cd20b637de4d3b7f8f028f36df46f003c9b0bb4c0826e1836a0dff99b919`  
		Last Modified: Thu, 01 Jan 2026 10:37:14 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:6e298551e9cd57d2082f54bca3d97bcbe0b8ec65eb968b11a81de95b1df482db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.9 MB (249858588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77bb7f6346e939d1e0397ff9601cfdae6a2967d27fecd463d1838fb24bfdb59`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 02:05:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 02:05:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 02:05:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:05:22 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 02:05:22 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 02:05:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 02:05:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 02:05:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 02:05:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 02:05:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be255ab5ccf8106b6424684700a41d5baa9ffc3f05ddc252ead95e6e46ebca94`  
		Last Modified: Tue, 30 Dec 2025 02:06:35 GMT  
		Size: 147.1 MB (147069816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af02edb872696285d0059648f5fda78473a16e7f45085331e954276b0b291bba`  
		Last Modified: Tue, 30 Dec 2025 02:06:19 GMT  
		Size: 73.0 MB (72953314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba514d7b4df23748f9fc44353b5612abdd8ddc7c1ff7697f4e53dd34cb78739b`  
		Last Modified: Tue, 30 Dec 2025 02:06:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69727ab2da9ac14dfcada379cf95ee8b0df3ef8a6a1574b7eedde25f5c70bf99`  
		Last Modified: Tue, 30 Dec 2025 02:06:14 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e68d55f270cb6807736dbbb202605e278393475b67aa8a737d4a7ef9d1a4904a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0bfa882c84ab3cf8a119585ab41e93547942e8d1d52643bd7a3b0d6ff83d73a`

```dockerfile
```

-	Layers:
	-	`sha256:e9b450569355b1115edfe3159a1679fa74b99cf98736562b068e2fa68e8fb5d0`  
		Last Modified: Tue, 30 Dec 2025 04:45:41 GMT  
		Size: 5.3 MB (5255225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c75782e05cdc1ee963d94967f9997be37c165ed5d79a2d0ced55c76c90886bbb`  
		Last Modified: Tue, 30 Dec 2025 04:45:42 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
