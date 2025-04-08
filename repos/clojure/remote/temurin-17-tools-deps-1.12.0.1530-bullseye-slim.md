## `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim`

```console
$ docker pull clojure@sha256:2c37a1c8326bf01abf2cfe8191913b99d77a850a9b479c25792f36db1f782c8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:2e1f9296396fd5794d2c02e5ee889ed94189b8ced985cfb3258dfe892f0b0aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233817372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3659bbeffe253244c18ede73c06278a6fda55e7f86924ef6197c19407d3cb54`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384928da5074ebbb01e61be8084d664629974b9f4e2c65abbf0cbad3448967e1`  
		Last Modified: Tue, 08 Apr 2025 01:36:24 GMT  
		Size: 144.6 MB (144566556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595a0d90b97a2917f0252aca1b432af82f77768d5d3395b0a0d85ff633562be0`  
		Last Modified: Tue, 08 Apr 2025 01:36:23 GMT  
		Size: 59.0 MB (58992357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f307dfeb6824964e0ad52fa7b4e737bf079be8d36c1428e70c577ac4cf2aae34`  
		Last Modified: Tue, 08 Apr 2025 01:36:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2c61395a8c3b1efb79ae40c236eeb05b76e535b4f8f9bcac296a9caff23ff4`  
		Last Modified: Tue, 08 Apr 2025 01:36:22 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f79b7ea96d55ce2c031d8e94f2e84aaaa576c40f2113c67f5d6d184098eac0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5134892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38282eadd9a08ad9febbae01fb1c7fd5e15c55bd8be951768ac6e0b399e46d96`

```dockerfile
```

-	Layers:
	-	`sha256:b1164a2c0d5946fdfbc09ae95d23a0222ef5938c83d2c3e6c4d8fb4ab091e145`  
		Last Modified: Tue, 08 Apr 2025 01:36:23 GMT  
		Size: 5.1 MB (5119013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f35ec1d62b520c85378284861b90919d36472d5f54cac4df5b15d2d59c9b1dc`  
		Last Modified: Tue, 08 Apr 2025 01:36:22 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a2cf1df1dbbe13616c66c95af647cff8616ee28570308bd5cd35c4cf1b4ee83c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.1 MB (231109885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1afe50a3876956a2d51c615289325d770357ba6f09c7470c5267bd23cc52fdf6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4714185560a3e233c84e342c5acf31dfcaa7f6f2b630be407160545cce8ab643`  
		Last Modified: Mon, 17 Mar 2025 23:58:19 GMT  
		Size: 143.5 MB (143454543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bed6a47da9f2d153d5e63d35223f6541c39dbbf4792c91cbf56f87386463c4`  
		Last Modified: Mon, 17 Mar 2025 23:58:17 GMT  
		Size: 58.9 MB (58908378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cd3ee4226739e5083e9eadbad304efa0f3b5417c1752a12833400c45e2e9978`  
		Last Modified: Mon, 17 Mar 2025 23:58:15 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5858a259a7920691e96be9460bb9138a2b10d5a2611e6ae6c767d097ba9e37`  
		Last Modified: Mon, 17 Mar 2025 23:58:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ff1ff127efe4a7c142188cac9db3ac1532af4dd0cd37f09a4d9d9c29763822ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10a96a3affc88aa2c71da158147421a2c4b555816caf4d5c6f94a4bbf3df5ef`

```dockerfile
```

-	Layers:
	-	`sha256:3c8b43cb25952587130c037a16bd670f74a19755434908d0b11bdeb1400132f0`  
		Last Modified: Mon, 17 Mar 2025 23:58:16 GMT  
		Size: 5.1 MB (5122799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f441212a89086e4366e34be160050ca9bdc467082d74f433259085eb44f1d20c`  
		Last Modified: Mon, 17 Mar 2025 23:58:15 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
