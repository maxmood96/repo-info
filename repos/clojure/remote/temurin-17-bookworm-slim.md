## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:f7af7fd71e4d9516710222c4a70517780f5797b7cfb570b19fcee4ede73c3a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:87a0d14c64b37e20327d3a5124191ae7550418b4c19fa4891cfc45834b6b6f67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243080694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f77813da1826ec0e81234c6c31c796ff064e54646fdef0943a45cc70e31948c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 12 Mar 2024 01:21:01 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 06:11:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 03:06:45 GMT
COPY dir:88c5118aff6896f6ed535dcde576d68ef88ded459cca013e0f9beb3e430ebb52 in /opt/java/openjdk 
# Thu, 28 Mar 2024 03:06:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 03:12:12 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 28 Mar 2024 03:12:12 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 03:12:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 28 Mar 2024 03:12:30 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 28 Mar 2024 03:12:30 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 28 Mar 2024 03:12:31 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 28 Mar 2024 03:12:31 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db34d09da7ef0b7c10d1180bf5afb0a7cc04cfc2fef22a109260b226f6f0804c`  
		Last Modified: Thu, 28 Mar 2024 03:24:38 GMT  
		Size: 144.9 MB (144893128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0756f809995c52602938d48d64d791de529dd23944c0bed05281c92ef1adce17`  
		Last Modified: Thu, 28 Mar 2024 03:27:44 GMT  
		Size: 69.1 MB (69062366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0372bbad73f37cc0783b04615841e99ec1ce56ae007eff9130d7f3d90b7b7fa4`  
		Last Modified: Thu, 28 Mar 2024 03:27:35 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822ba671f56cd5fb4a6e787ddcfe1046180a6e9f0e28f7c86d9e68ae409bf1fd`  
		Last Modified: Thu, 28 Mar 2024 03:27:35 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b7aa0d251fd912bfe726276787dd3511691d3a1cca77c46e8126a53ef180a713
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.7 MB (241695214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b14756a0d9920172521872f4ae6f38ceaf510e4c7c4152f4749aba956b9c4c50`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:44:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Mar 2024 02:39:31 GMT
COPY dir:a5d0039514ccd79689a0ea6094d70ca92113e8cbcc38d473b7c0fcc04a1f496a in /opt/java/openjdk 
# Thu, 28 Mar 2024 02:39:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Mar 2024 02:43:55 GMT
ENV CLOJURE_VERSION=1.11.1.1435
# Thu, 28 Mar 2024 02:43:55 GMT
WORKDIR /tmp
# Thu, 28 Mar 2024 02:44:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "7edee5b12197a2dbe6338e672b109b18164cde84bea1f049ceceed41fc4dd10a *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 28 Mar 2024 02:44:11 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 28 Mar 2024 02:44:11 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 28 Mar 2024 02:44:11 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 28 Mar 2024 02:44:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76dbb1a530d50bcec96fcd7bbb7abc3fb7a765a01bdf5b5dd96e07107640e6b8`  
		Last Modified: Thu, 28 Mar 2024 02:54:00 GMT  
		Size: 143.7 MB (143720921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a6b7c6c9544ed23aa0b49490fed427f74ee7f83825bb92ab4f465a8122a63d`  
		Last Modified: Thu, 28 Mar 2024 02:56:32 GMT  
		Size: 68.8 MB (68816845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b3357f219b4cd030b64c667342f83944e26267a4124122b0f4d6e275a9237d`  
		Last Modified: Thu, 28 Mar 2024 02:56:24 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee27aa864c025cb21e16e54087938420068113ed6be73d2eea47a103b30d9e35`  
		Last Modified: Thu, 28 Mar 2024 02:56:24 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
