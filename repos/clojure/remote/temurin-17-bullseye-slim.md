## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:24dd2a9aeb336251bf054dbb523a296ee28ce01acb0d0e1dbb66580a32d9cb8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:26330b0af8fa781545a90e2ff8e3e240b7fdfdc1f37e9105b3f5ca54e700c39e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234105252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab4d209ea453f94d1353127d090cca3eed30239f0dc5e8ff3ecff96d5d8afdc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:55:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:55:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:55:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:55:29 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:55:29 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:55:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:55:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:55:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:55:43 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:55:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cf5f39ef3fca9730ed04aee5f10040ea152a9793dec0d626f4205eeac5ec3fc0`  
		Last Modified: Tue, 04 Nov 2025 00:13:10 GMT  
		Size: 30.3 MB (30258596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79be98fb687e121c4b94b63da69b753e42ed435aac7ff2382de059a1d5aa738`  
		Last Modified: Thu, 06 Nov 2025 03:53:52 GMT  
		Size: 144.7 MB (144693306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e6fdaff639739f1c2b6219b0930b12a55219785441644227efb4474ca51896`  
		Last Modified: Tue, 04 Nov 2025 00:56:23 GMT  
		Size: 59.2 MB (59152309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d863e8cccd0ffc7cad9770f113b36e55971eb98f1feafcf84b4a5e24eb7ef270`  
		Last Modified: Tue, 04 Nov 2025 00:56:12 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047f423d4d9317302602bf1232ba6ba0b8dd379593af5454cad01e837eb1b5e7`  
		Last Modified: Tue, 04 Nov 2025 00:56:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:31e611723af0c9c58b5e128b9bf1804f8c85694b9515a66a50a42aeab7468adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5323902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef3ac8afede7ff9ee729d07847c6bb61e3775c2ce0540e30b2c90bf4f5d8ddd`

```dockerfile
```

-	Layers:
	-	`sha256:206a8460b0192f280b7c3a5d2a0b93c4acae9bd34e40c3eb4182969f716cd21b`  
		Last Modified: Tue, 04 Nov 2025 10:41:41 GMT  
		Size: 5.3 MB (5308067 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0387c742358d729aac93818353c90ded8000e830531e4b433abee897cb65298e`  
		Last Modified: Tue, 04 Nov 2025 10:41:42 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b0a6f8cbf8aed84566a44851c2e36d0ad4bc284234aeaeb8a1aac0523f3f30c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231579451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09c0e4bae25afab4405306644e2cceb52542eb7d2272cd6c1d963b3c16533271`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:56:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:56:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:56:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:56:01 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:56:01 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:56:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:56:15 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:56:15 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:56:15 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:56:15 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:241077dc995c26590e89ca59e622bf97509f2613a9e84e3e745225e4259eb511`  
		Last Modified: Tue, 04 Nov 2025 00:13:03 GMT  
		Size: 28.7 MB (28748552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:646be890758402262032c08fa000aa54b63e24cc4c224e904b427ecd7f56df40`  
		Last Modified: Tue, 04 Nov 2025 00:56:38 GMT  
		Size: 143.5 MB (143542093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b672d1eab369600014eb2a1a84e7021fd3ff2c123d731a871bc4fa3006d552c5`  
		Last Modified: Tue, 04 Nov 2025 00:56:51 GMT  
		Size: 59.3 MB (59287765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a664912bbd8e748a24f5cca52b721957d1a57ca87d3ab5458ce14dbe85896123`  
		Last Modified: Tue, 04 Nov 2025 00:56:44 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7bb8b9d808296ecce27e344d3d02e1bc9a69cc8ae5ccdfcfb3bc78d04084224`  
		Last Modified: Tue, 04 Nov 2025 00:56:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5adb1e8f0e575e75561cb564f75ba2de43cadf5482075ebf48900da9e1e58d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5329753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d3c8ac763acf5769b31f7f976cb3433548813a88eaa7e00ef03ba321cd759f`

```dockerfile
```

-	Layers:
	-	`sha256:defde574669071b41825791db9891770210eeea3af5882a4a8d52183e441618e`  
		Last Modified: Tue, 04 Nov 2025 10:41:47 GMT  
		Size: 5.3 MB (5313799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e740fa0ef9df0d2cb3d5280ccdceb8e60315fcc5a1ed7973d3ae2ba88af1efe`  
		Last Modified: Tue, 04 Nov 2025 10:41:47 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
