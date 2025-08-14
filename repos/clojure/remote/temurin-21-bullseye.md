## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:3e2fd9f79f0d488808806875bc666f051aff89ef8752c73af8043d659dcc5128
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5fdca331a02dd221f7717160ae139917104279763631fd3049db1e47bfcf7d9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.0 MB (280970887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea87e3a9072bae2301a7b7d09d0d9fcaba7b6c3b87be3ca88cdfa4ba254278e3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8782836297962ebca2e79ab2a9925fc0332c071c5a16228e68fb6f0ecee77e`  
		Last Modified: Wed, 13 Aug 2025 05:28:35 GMT  
		Size: 157.8 MB (157804754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc7f88fbc63644e637636cb179f3f28ee09dd6222136001690c129b14676585`  
		Last Modified: Tue, 12 Aug 2025 21:37:35 GMT  
		Size: 69.4 MB (69409750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5237c361efc46c59d7fc3943b6f6be445f06b7713bae1f8e5483d6b79985bce3`  
		Last Modified: Tue, 12 Aug 2025 21:37:32 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30984c7e27023a257a104b4b9102a9aa863c8144c37aea719b454f0cf7414db`  
		Last Modified: Tue, 12 Aug 2025 21:37:32 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1a0707c4c5e61d09f07ebbebbc9f643aa4e6756d78200e957ddcf52a036bd976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e6d7e2da050cf27c4c43d26b68590c98c4715d96097ca91951702e9879b077e`

```dockerfile
```

-	Layers:
	-	`sha256:1a3a68d004172906c7998a936b90abc317fc6346c47d7e77fef8c57fa4ea453a`  
		Last Modified: Wed, 13 Aug 2025 00:38:31 GMT  
		Size: 7.4 MB (7399416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb3599b0af7298fed69ac23c4b8aefa0364f62db8909674788d0af2a99874ea6`  
		Last Modified: Wed, 13 Aug 2025 00:38:32 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0a828c8057e9afa0e2b17cfa2a3becd58d6f141987dacb7833ce1b95ef33ae15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.9 MB (277868204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e838fd510fd4a1a42c2c9667576c40b5dd0d5af610aee4fad73f8bbb1803c0f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38189cce6557a4a815df98951532ae448e878aef481754a77d268892737a72b5`  
		Last Modified: Wed, 13 Aug 2025 19:04:55 GMT  
		Size: 156.1 MB (156081249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7adfe31749f4fb231dd7dac9e1a5f63ac1bc154909161987f65d025fb25ee9e5`  
		Last Modified: Wed, 13 Aug 2025 14:37:42 GMT  
		Size: 69.5 MB (69537508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19842f4299db8248d473bb896bfa774911ea6d478222ff95b8b924875793eac6`  
		Last Modified: Wed, 13 Aug 2025 14:37:39 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6014ecc7022a8c70cf7eb113b9dbd38f69bdc4c0f687997aade73fda6ed65cfb`  
		Last Modified: Wed, 13 Aug 2025 14:37:36 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:208af93e31268d3973198eb0749ecc57423b48ce3788d0d71f014541d04d933e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7421178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab8de921c634a6cb17f48d195ebc5eac6809c6ba2b37c0a2bdb5259568edb4f`

```dockerfile
```

-	Layers:
	-	`sha256:052a38efd17351342fd3545d6bedcded8df19a995ec89c0d2c29b17b1875f49a`  
		Last Modified: Wed, 13 Aug 2025 15:38:55 GMT  
		Size: 7.4 MB (7404539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d50320661eccf9d9d563939f3b637b74bac9953d7ef441a4339218727dfd2185`  
		Last Modified: Wed, 13 Aug 2025 15:38:56 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
