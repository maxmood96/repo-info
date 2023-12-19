## `clojure:temurin-17-tools-deps-1.11.1.1429-bookworm-slim`

```console
$ docker pull clojure@sha256:4311480871fa51620e50c0b980bf12e5ca4bb4dc1e26caab95ff84bc7d32cd4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1429-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0b93d975602030084eec3e08cdfd71d6b1e15aa60f7e0ae4f3a806b54c34fdeb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246145644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c90813f23f5c6de28edf2cd05ddec531b927c50c15a47b7a9ba3e3b1ff4ac45`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:20:27 GMT
ADD file:ac3cd70031d35e46d86b876934946ffc8756de4de065fbc926dce642dac07ff3 in / 
# Tue, 19 Dec 2023 01:20:28 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:53:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 07:04:40 GMT
COPY dir:49a2e688f44261aae915217f8e2f904bd2f648eb9b4304aa7acb2d17c036311c in /opt/java/openjdk 
# Tue, 19 Dec 2023 07:04:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 07:08:29 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 19 Dec 2023 07:08:29 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 07:08:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 19 Dec 2023 07:08:48 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 19 Dec 2023 07:08:48 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 19 Dec 2023 07:08:48 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 Dec 2023 07:08:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:af107e978371b6cd6339127a05502c5eacd1e6b0e9eb7b2f4aa7b6fc87e2dd81`  
		Last Modified: Tue, 19 Dec 2023 01:24:59 GMT  
		Size: 29.1 MB (29125963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ae9ec6c61b4668ec9e593fb594df2ba1f507eec15ec26cc6c05670cb147b4e`  
		Last Modified: Tue, 19 Dec 2023 07:21:58 GMT  
		Size: 144.9 MB (144873901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfa422b5974105a1827cfb4b084cc002238653e5f2e7718155cbf0aaa1aebb1`  
		Last Modified: Tue, 19 Dec 2023 07:24:00 GMT  
		Size: 72.1 MB (72144766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cee3e4d497e6f72a930b63cef01f8a2b81c7472f53a49643906ec743c6f1ea`  
		Last Modified: Tue, 19 Dec 2023 07:23:52 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e51eb99395a247f5d2716e4dbe148899188c60c4df3925fed18143a1f51b811`  
		Last Modified: Tue, 19 Dec 2023 07:23:52 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1429-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:11f36682c9dc1994080ad00228109fc3fed71332baad4c6ebbca20c61e290cb4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.7 MB (244724429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f05571e9678f39c29df0f0d082e0a6a76ab5a34ac8d2de33a5f5027a7512e75`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:54:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 Dec 2023 07:04:08 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Tue, 19 Dec 2023 07:04:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Dec 2023 07:07:17 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 19 Dec 2023 07:07:17 GMT
WORKDIR /tmp
# Tue, 19 Dec 2023 07:07:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 19 Dec 2023 07:07:33 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 19 Dec 2023 07:07:33 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 19 Dec 2023 07:07:33 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 19 Dec 2023 07:07:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ee60140f19529393a1624031eddbd14b1675cecae82a1f83a9055965ebb645`  
		Last Modified: Tue, 19 Dec 2023 07:19:05 GMT  
		Size: 143.7 MB (143681714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86ab8f3b2cbc35f8ce7137411400b969740debe6630e723526edb60d70520f7`  
		Last Modified: Tue, 19 Dec 2023 07:20:53 GMT  
		Size: 71.9 MB (71884434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fcc447fb7b1f5ea8d4f81a0dffa42df2b709ad22a2471c4c15b6c543a3b5728`  
		Last Modified: Tue, 19 Dec 2023 07:20:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468430cf37fd62cdf7fc53ec18b412181415ab49b72553ece8275f4659430e5f`  
		Last Modified: Tue, 19 Dec 2023 07:20:46 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
