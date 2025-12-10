## `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye-slim`

```console
$ docker pull clojure@sha256:b687fb1df355be294f1fdaf88bd6ca85a0b0f5d30d56019db1d942cf89d640fe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:431901c7fbfaa03115bd3c7eb98fdab4f3c8004f29716aba2cf8a7857c419cd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234259544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a0e50975750e353fcec7998b2494940640ae8ebfc3669868cc2c4173e901f7c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:53:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:53:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:53:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:53:41 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:53:41 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:53:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:53:55 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:53:55 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 08 Dec 2025 23:53:55 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 08 Dec 2025 23:53:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a88499d92e58a9f7d74dc939bd949d9c2d87abbbaaec03b5f87553e69d901a53`  
		Last Modified: Mon, 08 Dec 2025 22:17:50 GMT  
		Size: 30.3 MB (30258465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41762d16e0636abc03eb1b187d80ada18581de13cb19ffbc7b50cc8a0631d83`  
		Last Modified: Mon, 08 Dec 2025 23:54:45 GMT  
		Size: 144.8 MB (144847951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219bf28bc46b7cdf6c7c154062f9833182cd473a8aae883e650f9534d3f4730d`  
		Last Modified: Mon, 08 Dec 2025 23:54:26 GMT  
		Size: 59.2 MB (59152086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e07fc6db3793398af89348726d36abab6535b8ee7bf0ae5d21954950131e59`  
		Last Modified: Mon, 08 Dec 2025 23:54:22 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4def3b863443c0dd561f29cff75e20e464c2c4f64310345858845925d23a81`  
		Last Modified: Mon, 08 Dec 2025 23:54:22 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d31045748c63ae64c4105b74c81ccdb4290d905441e3375a44465fffb8315b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5323904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b388a866e821a0a6ee8f13c4296984d63f0a7569bbfcadc4b7622a26c80c5bf`

```dockerfile
```

-	Layers:
	-	`sha256:3a24934a3b96253434d7a8bb4e1cce08ec377dc1e717e9846109de9f4e28a383`  
		Last Modified: Tue, 09 Dec 2025 04:39:28 GMT  
		Size: 5.3 MB (5308069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f91c8fa813d7fbcc4d51569d5106cc5cf15212209525755d6d78e5c7c297f23`  
		Last Modified: Tue, 09 Dec 2025 04:39:29 GMT  
		Size: 15.8 KB (15835 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dddb10e192a875e81d2848249c6d89636dc3c560a2792c13d7926b18cb6f6d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231717169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:252041cde40a10ef2c514dad109badb0f7ecfedc8dceecc21057a6d353df34b1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Tue, 09 Dec 2025 00:01:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 00:01:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 00:01:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 00:01:15 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 00:01:16 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 00:01:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 00:01:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 00:01:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 09 Dec 2025 00:01:29 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 09 Dec 2025 00:01:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7d43510e20279c4831f5ca1d424a1d56c6c24251d7c93288a50a066dc7e72bda`  
		Last Modified: Mon, 08 Dec 2025 22:16:06 GMT  
		Size: 28.7 MB (28748482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c8f04d6f4d370d29dd21be7673edeb1526deaff3f8ad98117c137070466bc1`  
		Last Modified: Tue, 09 Dec 2025 00:02:08 GMT  
		Size: 143.7 MB (143679914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5d93094e4dcf2792ddfe7e140aa28ede743a74670e5d8568753e669d94c4f3`  
		Last Modified: Tue, 09 Dec 2025 00:02:02 GMT  
		Size: 59.3 MB (59287733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d173ca9a365ef298ec3f471564de9736b5a4b92612dd786a9b3c948d4de8a2d0`  
		Last Modified: Tue, 09 Dec 2025 00:01:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bd91c58481c1a5df6ea5ef4c1757d93b6bb907967583f625113e156566a4e6`  
		Last Modified: Tue, 09 Dec 2025 00:01:56 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c72e10f26890d7465c11c1590b24b5a2082740e558d79e33b93a7a6a0db50948
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5329755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd9aeadd9e099cca55af7a0260b62d0a475535d04e210f3c510e9c168f06d91`

```dockerfile
```

-	Layers:
	-	`sha256:ba1395d3b4d65bc58ca8c24fed7c0d2f3c5373f5121ae1b203190b0e98519d6f`  
		Last Modified: Tue, 09 Dec 2025 04:39:33 GMT  
		Size: 5.3 MB (5313801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e47e6bf5ff736051778153bb3fd8111e1031002a5f652a0b42be34d77bdc1f7`  
		Last Modified: Tue, 09 Dec 2025 04:39:34 GMT  
		Size: 16.0 KB (15954 bytes)  
		MIME: application/vnd.in-toto+json
