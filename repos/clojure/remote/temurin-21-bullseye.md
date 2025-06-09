## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:394f61b3b877bf8cd06c988aed176137c88b26155fde3872235c58e7a3b9018a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ddd088e283fdfe9fb1f2095ca69c7dce03d6e04d95bf4d179674c59fe6c3e031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280795590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24bdceb13d0caacf05c9078f1df9b5244a9d3d7d65615968a5ab64fcbaec1fc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:54107f2de180b7b6e9f909d2f1c6c18e10c700a6bd80a035d931768b06bb2905`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 53.8 MB (53750195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b7da8d6a161e1601a6dd7c4386328e86ae38174f8cacc303174b7e79bd122fd`  
		Last Modified: Mon, 09 Jun 2025 18:58:42 GMT  
		Size: 157.6 MB (157634503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e33048654b06fb2fff2dd8edd87bfdc4a2b05207ec1675edec4dbfa0ba0898a`  
		Last Modified: Mon, 09 Jun 2025 18:58:40 GMT  
		Size: 69.4 MB (69409849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a512d823b7578b45e28b87a33b6c7514b295ade986e692988e80ab018409f53`  
		Last Modified: Mon, 09 Jun 2025 17:19:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b433ebbd7db913bb58e795f9e49d4e1d1d5102ba586e62d387ab92955e22d343`  
		Last Modified: Mon, 09 Jun 2025 17:19:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6fd6ca5c563647d604bd6d806dea341ede62882622a3410ced99ef5b8b4db55a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7417537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fff535169ebf89a491487e2c6c03f431ff753f704cf5aaa3409a0f38ea5968a`

```dockerfile
```

-	Layers:
	-	`sha256:09b53083ce95a6ed925c42796baf48630137101952b688d8e38e0dc4cc3bf2c9`  
		Last Modified: Mon, 09 Jun 2025 18:39:10 GMT  
		Size: 7.4 MB (7401040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:276fc85a9ba1223c4b0765dcaee8ed62b7b0189683518d5bc4adab3cb492bc16`  
		Last Modified: Mon, 09 Jun 2025 18:39:11 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b41c183edfa628df2577e3421c15df65d6caa94fc42c2a7f26bec37f7e53f4f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277715487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48f4b58c4b7a48b30cad5c5759d059e59e62e27abb96d91d597f7e6c7bb649d7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
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
	-	`sha256:b2737025fe8da5b868f566cb4e3dc3330028cee06c83db854f56467eca6e09b8`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 52.2 MB (52247755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a5e26e3cb5abfbd307a69d846765430705dd9214f5910e9a937311871d3dc9`  
		Last Modified: Wed, 04 Jun 2025 12:44:46 GMT  
		Size: 155.9 MB (155928831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4f8352ceba8fc0b8d3c4194bb0aa338dbdced1d51b9d2086648ca13db4980a`  
		Last Modified: Mon, 09 Jun 2025 18:59:03 GMT  
		Size: 69.5 MB (69537859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a235369774b1893ac10b7bb4772c9de399687f197cccc773f5849c11421ea25`  
		Last Modified: Mon, 09 Jun 2025 18:00:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921123a56dd14c85e220aa9939ff184240c5946503d3f265191280a5e829ef95`  
		Last Modified: Mon, 09 Jun 2025 18:00:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:32459af2cbabfbac8f6342723118a36bf96edb78320fb2cee13018e4db04f9cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7422802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550995c2abbd329e42bb1e01557a5392c08915d3ffc3bc71699406492cdff450`

```dockerfile
```

-	Layers:
	-	`sha256:f98039738ec2a03b7c234d1cc2fb57f27353be158feb6f6483704643f105841a`  
		Last Modified: Mon, 09 Jun 2025 18:39:17 GMT  
		Size: 7.4 MB (7406163 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89ed8f3e8a73e6230f802a6326172ca416669208262819374d1093e1290ab92e`  
		Last Modified: Mon, 09 Jun 2025 18:39:18 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
