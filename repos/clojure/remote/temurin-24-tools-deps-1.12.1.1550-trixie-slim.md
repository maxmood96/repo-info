## `clojure:temurin-24-tools-deps-1.12.1.1550-trixie-slim`

```console
$ docker pull clojure@sha256:162b165364f749760ad950077aa9338f08fdb99ef959d57066240020305eba02
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e2459087d1888a5b385da5c1c1f108afe2a4b8af02343396ef331c3209a265f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194373098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c86450ebdc76605201dd3f1e1a04c7b2dd9875007841edf640809f0e1fbc8e78`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
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
	-	`sha256:ced038dea045df288fe9bdbe03117ca66fe2a071217e196ac86ed07f965fe688`  
		Last Modified: Tue, 03 Jun 2025 13:30:48 GMT  
		Size: 29.8 MB (29755384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe04acabeeefac7b5e36cf8934992f3c98562a2b42d0d500e9ed49161bc26d4`  
		Last Modified: Mon, 09 Jun 2025 17:19:32 GMT  
		Size: 90.0 MB (89952019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf31998a57078d637e45d6e9eafe1691fc02adbfb5d6bc00f2b57a0280bd4d4`  
		Last Modified: Mon, 09 Jun 2025 17:19:28 GMT  
		Size: 74.7 MB (74664655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e444a77fd61dcc9fa004ecab5c16a411cf3cb2e853eba8f9fdd432162a54fb`  
		Last Modified: Mon, 09 Jun 2025 17:19:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619f347f805e0cebfa412896edac87f39965b009f766f8586d1c2434994782c7`  
		Last Modified: Mon, 09 Jun 2025 17:19:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b22eb1cd32b0e301dead1914e8e58636f1bd2aecd769b70ac911a1312e71559d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a22da23b77d42a60b7e0cbfe6f027aa62c51227975523e34ffabf14415970b`

```dockerfile
```

-	Layers:
	-	`sha256:92485adb403140cc7972c3fb46fdf8852674f3a08e369e8c602cd183e81e330e`  
		Last Modified: Mon, 09 Jun 2025 18:42:01 GMT  
		Size: 5.2 MB (5202930 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cef2109610214aa04613c5b0fa638bd5f52d34b68afec110790a690e9a8058f3`  
		Last Modified: Mon, 09 Jun 2025 18:42:02 GMT  
		Size: 15.8 KB (15847 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7cebeacfa5bd55b25eac1beaedb2bd979c9126a2013a9b9931b56651af2f6c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 MB (194179065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:144c8c34c13b8c04e950a4638d7f2aa5fccd3489252ab91732452eb23caf0a56`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
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
	-	`sha256:6098c2c9fa277c00ab580ce12bf64a9e1edf9e9139ba18ad85f3cc3063834aa6`  
		Last Modified: Tue, 03 Jun 2025 13:33:56 GMT  
		Size: 30.1 MB (30119455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9eae18b910302d512424dc442cd7d56bf789911ad2568ced024da733788c71`  
		Last Modified: Fri, 06 Jun 2025 12:13:25 GMT  
		Size: 89.1 MB (89091283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0b38b5a2d2bc1f732a90620c22adf379f1a75f5c90fe9570ec412b0fc1b71e`  
		Last Modified: Mon, 09 Jun 2025 18:03:50 GMT  
		Size: 75.0 MB (74967284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f10e998f717f330d51060b0c5956f17aa7df01dfa0beb07905d935f0e4fd649`  
		Last Modified: Mon, 09 Jun 2025 18:14:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8973727016970b69df3a0721f95accad080a678e0362f5938fee406c3f01048e`  
		Last Modified: Mon, 09 Jun 2025 18:14:44 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:76b94288095bc19376a40086856766006cc3c4aa09248cd4c0c14267010c01b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaeb1d98be07a46d63741c72cdf1cc2ca7a3205e61361954d1a7f8aea7f177bd`

```dockerfile
```

-	Layers:
	-	`sha256:640ff86e2a7a8e9298f3c1b923478b57f6737422b80477d1ab010629dad91a7d`  
		Last Modified: Mon, 09 Jun 2025 18:42:07 GMT  
		Size: 5.2 MB (5208696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88655a97fa42c579118580cbbd37b322bbebe50d36e9a97f488239ddeb7e242a`  
		Last Modified: Mon, 09 Jun 2025 18:42:08 GMT  
		Size: 16.0 KB (15966 bytes)  
		MIME: application/vnd.in-toto+json
