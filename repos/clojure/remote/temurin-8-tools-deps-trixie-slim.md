## `clojure:temurin-8-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:f17105f3536f106be7bad56cf7aede3d540e467d9bbb530e1928556e7b657dbe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3eba95a858370740cf66a434dafeaa80bff14fe6670ea67e94633bd52ec270a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.9 MB (159923873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01b8af23ed928a0c77aaff7cc86e9d5388e60e56b971e6b909d2cb87afb1eae`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:01:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:01:06 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:01:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:01:06 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:01:06 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:02:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:02:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:02:08 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b39c97740c91198b20f39caaeb1dae1242992552b706e1239290da40f94959c`  
		Last Modified: Wed, 15 Apr 2026 22:01:38 GMT  
		Size: 55.2 MB (55170060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f17135b94c0feb808fa06bfbdb2568b93461b4825d702e58d379b312c248cb`  
		Last Modified: Wed, 15 Apr 2026 22:02:25 GMT  
		Size: 75.0 MB (74977528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77091012733b6d424e727ecf6b376096848ca3c7f41c26741485d7524af86d93`  
		Last Modified: Wed, 15 Apr 2026 22:02:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8cf5b3f29b04de3775eb065c848396dbf6d3468da4fc8b17b4575341e4daabc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5393553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c87d99c3670bd3e1688db8a51f4e19b91ddeae5ab65a041eaa407ffad205def2`

```dockerfile
```

-	Layers:
	-	`sha256:ef5a2267b3bae72d57bb505c8550e60ba0d7ec4650f27491d6e55ef032410d56`  
		Last Modified: Wed, 15 Apr 2026 22:02:24 GMT  
		Size: 5.4 MB (5380125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac0c86971696e530cc14b539cb3755da8202092742960d5527828aeb7ac69e5d`  
		Last Modified: Wed, 15 Apr 2026 22:02:23 GMT  
		Size: 13.4 KB (13428 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b3e7bf1af3d24b4d6be3d5db5b562933fa7727798f654bff8d86086eb92d1054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.5 MB (159541476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16061fca035b7a197cb866e419dfb83dc752ea3675da0d79b562495602b51c8`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Wed, 15 Apr 2026 22:13:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:13:14 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:13:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:13:14 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:13:14 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:13:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:13:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:13:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa7233c97e82f19cb49834fd0e394ce5d99809e88b5ebdd6d918776e9b7ea28`  
		Last Modified: Wed, 15 Apr 2026 22:13:54 GMT  
		Size: 54.3 MB (54251614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ee4855da2171f34f759903cd43e4b3390108de96f5b27f3b817199cc7ff792`  
		Last Modified: Wed, 15 Apr 2026 22:13:54 GMT  
		Size: 75.2 MB (75150666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f991ef264bed68a1bb517f2344618db73160b851f533b55afdfe082f77f7dd`  
		Last Modified: Wed, 15 Apr 2026 22:13:51 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:037f6d21cb2563b44dd061091b4ca89e8ca885113125bcc6e53baffdd99e6d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5400938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c13dabb7dc1dcc29c88cbdd3224ab4e944b2b5f688d1010a615b9a5d4fcb482e`

```dockerfile
```

-	Layers:
	-	`sha256:d3802d108cb23cb2c798b33caeb8fcb18cabdea2ed4f28bd85c45951a8b90539`  
		Last Modified: Wed, 15 Apr 2026 22:13:52 GMT  
		Size: 5.4 MB (5386594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab3b9c29b3ac310ca499f9a12dacbbb8cb2b0f08090fa95b26fbc607822f6b74`  
		Last Modified: Wed, 15 Apr 2026 22:13:51 GMT  
		Size: 14.3 KB (14344 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:e36488e139adf5c00693585cfa3a31d8cb7f9b2bd7ce6801f678680bb0b83220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166854684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1da4113dc7ed714001c078a5ffb26f6d2d391f5b3b662b65a2a15d40abf296e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Thu, 16 Apr 2026 02:33:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 16 Apr 2026 02:33:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 16 Apr 2026 02:33:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 02:33:49 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 16 Apr 2026 02:33:49 GMT
WORKDIR /tmp
# Thu, 16 Apr 2026 02:38:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 16 Apr 2026 02:38:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 16 Apr 2026 02:38:53 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e63a89287f0e4231d910962450035b1c85dad03ac1f8a55f7f7733aa2a3a02`  
		Last Modified: Thu, 16 Apr 2026 02:35:04 GMT  
		Size: 52.7 MB (52650393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17a79b5c651e8484032717a4efc983611dcc6018320fe2d2eb60beb593d1948f`  
		Last Modified: Thu, 16 Apr 2026 02:39:26 GMT  
		Size: 80.6 MB (80610629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9cbbd62fdcd7b35fadc082fdc4bb27317c175d2a41980ceaa6f17cd69f61dea`  
		Last Modified: Thu, 16 Apr 2026 02:39:23 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:92ad58f121f5b0e23dd8365364bcbdc5e9f5e112828b400c066dfe2b8ff0fd35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5399366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beda76ec5b1fd5a24eee91dffb276a70e5c4f02c39541a962368dfd5d4ba0b02`

```dockerfile
```

-	Layers:
	-	`sha256:73078a9199ba91f8c158b8566e2a523a3ae117bfba2267f729b3f6e81ab83b0a`  
		Last Modified: Thu, 16 Apr 2026 02:39:24 GMT  
		Size: 5.4 MB (5385091 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e23ddef9731fe12df5fb50f4d758f970cd1fe517eb8f3aa3a1a2eb43ca8671e6`  
		Last Modified: Thu, 16 Apr 2026 02:39:23 GMT  
		Size: 14.3 KB (14275 bytes)  
		MIME: application/vnd.in-toto+json
