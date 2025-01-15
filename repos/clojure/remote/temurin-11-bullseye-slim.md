## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:71012f06c08fbf4699272d61fa83599ef3086cd0bec8db95cba2b8a72d881c6e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cd7f067ea4c625b949363e035fb981e47a4daa3542df64fdce939916a5d6d034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234635796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:164953a4a672fef1589f8c8e855697b6d625564d163d3eeb863b5b151a5984f9`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 20:33:08 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edc547c4158cc346c8697ae863b3d20efd7dfdd3ed7051fe11db6797199383e`  
		Last Modified: Tue, 14 Jan 2025 02:44:29 GMT  
		Size: 145.6 MB (145601500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c89e038dcacde33c08029a6133069de1a9649ccaafc1d00573786910236dc62`  
		Last Modified: Tue, 14 Jan 2025 02:44:27 GMT  
		Size: 58.8 MB (58780987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3a82894f69d33b533da2ddf60c9aa1d30c43647e0fce2b1b2ddd9c88b8587e`  
		Last Modified: Tue, 14 Jan 2025 02:44:25 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:67eec1db9ec7a027fa9c997219386ba7b87edafaa8c4376ac4786681a99bbf56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5151518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db8264e272e8365214aa1c8f776157b6b0626d4ecfa61a6d731e8a7e651f8e64`

```dockerfile
```

-	Layers:
	-	`sha256:6c3485c8b8e3c634f9010f528bb67d2957725ad9630d0a653750c85f4d33f848`  
		Last Modified: Tue, 14 Jan 2025 02:44:25 GMT  
		Size: 5.1 MB (5137208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee536552b0941fca509e513208d449e2c934a57a2ffc4e04cc02eca4d8cfcb95`  
		Last Modified: Tue, 14 Jan 2025 02:44:25 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3209a30ea25250f44c376de1b783caf749f4072e37c8aef1c8653d3983cacdc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.0 MB (230039834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6977ac70fa222e8dd70c36940f4f7cae308b3ae5ad75d5803fefc61b4b8aee1b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28cf82db26d86501260672c54fc7020ba090a01bdfde566c71cdb90838bf1a0`  
		Last Modified: Tue, 14 Jan 2025 07:27:47 GMT  
		Size: 142.4 MB (142389022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbbc7bab8932d7ac1d0ec8a7ea3bcd3889aed5c2bfc7a7a1b7d52ecb8d6e22d`  
		Last Modified: Tue, 14 Jan 2025 12:25:56 GMT  
		Size: 58.9 MB (58905255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4093b6fe79b987620be9c1c347bd4dc8fccd435c7e6e45c4f0369248329d619e`  
		Last Modified: Tue, 14 Jan 2025 12:25:55 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1082da0c64642315794658d382a257611a0c20f7ca6b727a860e42459b4bb7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5157986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eec44d8611e554092f21aacdef266980bc60fe3540f6aff0dafa2d8b54bc8ba`

```dockerfile
```

-	Layers:
	-	`sha256:0eab688ce39f7631988ff30346c2a62f40b70a5eb945389e60b6069c0611371b`  
		Last Modified: Tue, 14 Jan 2025 12:25:55 GMT  
		Size: 5.1 MB (5143558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c4a0fc19a8bf0a2dc4e9576b6e903905e3d4cc9597644c89894f3b65f49c6ea`  
		Last Modified: Tue, 14 Jan 2025 12:25:55 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
