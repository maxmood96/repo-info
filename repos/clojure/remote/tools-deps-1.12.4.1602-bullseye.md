## `clojure:tools-deps-1.12.4.1602-bullseye`

```console
$ docker pull clojure@sha256:3e6e727d029d92dca9868f7fb833a6ba7794cac07e76001fff3e1fb1ed8c2642
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.4.1602-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a19ea474e1f8937c6c20a241a0c6a43e41903b1a6119aa7fd3907fbe67f6b63c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.3 MB (215344339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba75c17b647be20b843dca4e7a190542d327aa5f2e3bd0b1ba3028f7958acfb1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Tue, 03 Feb 2026 03:22:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Feb 2026 03:22:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Feb 2026 03:22:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:22:46 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 03 Feb 2026 03:22:46 GMT
WORKDIR /tmp
# Tue, 03 Feb 2026 03:22:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Feb 2026 03:22:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Feb 2026 03:22:58 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Feb 2026 03:22:58 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Feb 2026 03:22:58 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb35b305ff7c52dcb63e19672dd2bda3fdda23b2462d7b2db5c5992008247b6`  
		Last Modified: Tue, 03 Feb 2026 03:23:19 GMT  
		Size: 92.0 MB (92045314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1672eae01b34f9db5a14490b460c5364bea894965c2f04ec86d4f7f3fb3e681d`  
		Last Modified: Tue, 03 Feb 2026 03:23:19 GMT  
		Size: 69.5 MB (69541725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94936744e59ebc4ddbaad2a79a46b921f6eca0e01c0f608c8be716d5de43abb`  
		Last Modified: Tue, 03 Feb 2026 03:23:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcf7e0c5f9d8c93b0689838c8f0da12818dc2002c921a665a812df0618d313a`  
		Last Modified: Tue, 03 Feb 2026 03:23:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:28155660df16502b787977f9d26dab7153d19473a23d171477a653f858a814cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7364253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5938307d010680be9c195e5d75ccda6b8a83ef289642b9a94343f2004ed364e`

```dockerfile
```

-	Layers:
	-	`sha256:6c5618448d852e31ff09fd9f18ce8b5356c4d0b66324fa004b99fd82d1e735d8`  
		Last Modified: Tue, 03 Feb 2026 03:23:16 GMT  
		Size: 7.3 MB (7347806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62204fa02486223dee94e0c3c1bebb14d05b9158ac04ed90a272816e28a8afd2`  
		Last Modified: Tue, 03 Feb 2026 03:23:15 GMT  
		Size: 16.4 KB (16447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f58c1b2837022a8efe07ff987c875fcace70ac85d58d09d79241a9b7ba42c725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (213004508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c560e7a3024324a9731d2c70f14c4fb9f19e44e8c9a5b2281239c8755d9b140`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Wed, 28 Jan 2026 18:06:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 28 Jan 2026 18:06:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 28 Jan 2026 18:06:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Jan 2026 18:06:22 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Wed, 28 Jan 2026 18:06:22 GMT
WORKDIR /tmp
# Wed, 28 Jan 2026 18:06:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 28 Jan 2026 18:06:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 28 Jan 2026 18:06:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 28 Jan 2026 18:06:36 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 28 Jan 2026 18:06:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0c9029c19a9aa67ff2b1313f591bcb473f0522775cc5a54491b5f7754253c547`  
		Last Modified: Tue, 13 Jan 2026 00:41:31 GMT  
		Size: 52.3 MB (52257769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7bed2ea4dd2853df75e6f7b73ef2b107d4f43de151de10d4241b39f537d0de`  
		Last Modified: Wed, 28 Jan 2026 18:06:57 GMT  
		Size: 91.1 MB (91052493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6834347a771aa5bd453fdfd16e11fa45d51549198d1b299d06d700bcf593f9`  
		Last Modified: Wed, 28 Jan 2026 18:07:00 GMT  
		Size: 69.7 MB (69693206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff0ae471303774a93dcd9ea339a970ef50c1623d6256c99891394c1ba0b8dc19`  
		Last Modified: Wed, 28 Jan 2026 18:06:55 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddd4d1bede5c5fc709678d62618f221aacbea73e298be4be375866e981cff4a`  
		Last Modified: Wed, 28 Jan 2026 18:06:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b0c8c4b5fd1bd63514b68d28bc46e6741f9e7f81e8800f7bcc1b300965c95969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7369514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68648e20d2903ebd9fc826f96a0ae152ab3bb9938bd6d1ac5c34f9f813ed41f7`

```dockerfile
```

-	Layers:
	-	`sha256:fc2f57cc69ef646f71fc89f10e7355a7a6d357d19646a3ea4d92a7a90f11d928`  
		Last Modified: Wed, 28 Jan 2026 18:06:56 GMT  
		Size: 7.4 MB (7352926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc2ebe55412d704900519cd05aa1ced558059a9ff15f4a1956965a9a79eb6b91`  
		Last Modified: Wed, 28 Jan 2026 18:06:55 GMT  
		Size: 16.6 KB (16588 bytes)  
		MIME: application/vnd.in-toto+json
