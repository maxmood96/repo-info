## `clojure:temurin-24-bullseye`

```console
$ docker pull clojure@sha256:7b05b31120c4358cc6f1a5535cde14c60a080b9da4a6c85f1d914596d8a5ee0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:604932363a810bde8009533b50b70826024bc2f8a9cabb01bebe8175b6b94967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.1 MB (213101492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d43ea5de887f49c1cffd3253586e12483ad1a80f997cb2162be2b50fceca6f5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30fcc19a67f7c23934d4a55148b82ba9143aa778f81d154eaed249b614c1116`  
		Last Modified: Tue, 03 Jun 2025 05:17:00 GMT  
		Size: 90.0 MB (89952002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4cc8937861d21162cdae93e7dad1f66c8961ec395353acbf957ee181d638e6`  
		Last Modified: Tue, 03 Jun 2025 05:17:00 GMT  
		Size: 69.4 MB (69398257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e5915d6d84be2d7e923db732c42376f9bc4cf1dc08611d904d819afaaf4524`  
		Last Modified: Tue, 03 Jun 2025 05:16:57 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55093a0f991f40d56a7da4e780840f4282539463be476bd3eca3e23882bba8ea`  
		Last Modified: Tue, 03 Jun 2025 05:16:58 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4dbed1dc5dd1c1c1f93cdd38f3034ed8e2971ee151a1fb988440bc1c7f1735e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7222646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e997156d17e32096cb67e8f36f690278ad15a2e2f35260326d568de2aa93cd75`

```dockerfile
```

-	Layers:
	-	`sha256:c062656e2dd4e7c7ee07c26be4b5f609d4ecfb7ee2d22b7a689fe9c3b52b775b`  
		Last Modified: Tue, 03 Jun 2025 05:16:58 GMT  
		Size: 7.2 MB (7206832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2789a0be32c9aa7d111aa2f664a1c0f844fc0c99c1fb682c8278004d2c04e57`  
		Last Modified: Tue, 03 Jun 2025 05:16:57 GMT  
		Size: 15.8 KB (15814 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:581ef7e073a5bb7f690ab4cfe6768a2f1f21a5e00c4cc8fcc6851c721fec6da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210870715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc82813832689d322ab333972ae953539d8a8bf1cddedeef8e9af4a9214ef149`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e138a1071d10d13cb8382959f5fbc892b4601755504e76a2d09f248081aa2606`  
		Last Modified: Tue, 03 Jun 2025 11:06:45 GMT  
		Size: 89.1 MB (89091274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d9fcef2bbcd6d227594a4c425b98e8187a77816aca855afb208c732325d48c`  
		Last Modified: Tue, 03 Jun 2025 11:12:39 GMT  
		Size: 69.5 MB (69530643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9ee314457f16387607fd2e6920513b40f4b69465b5ae7f731856a03176f023`  
		Last Modified: Tue, 03 Jun 2025 11:12:37 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01fe4b65fe876f1a2ce416bdae747e8501a1072e4095003f9609d5475ed58dbc`  
		Last Modified: Tue, 03 Jun 2025 11:12:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7288bf8254a7fd501ce2aeb1df3cbaa354b0bd349b68080b927a56305f215656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7227860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2a2de369d34b06a2f9bc90a6e654b99b38023a1439bae4cb7e4e77e02386b1c`

```dockerfile
```

-	Layers:
	-	`sha256:8ffb3f6fb6bc80579d292f148e1ea25073742a5e40a20f9d7ff917a355f4ed87`  
		Last Modified: Tue, 03 Jun 2025 11:12:37 GMT  
		Size: 7.2 MB (7211928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1efbefe6dcaff3a0e37773c178fabe09673db8fa76ec4ba95f7abb29d12f0938`  
		Last Modified: Tue, 03 Jun 2025 11:12:37 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json
