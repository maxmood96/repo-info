## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:4f8e017364feb18eff6802f8182febc201a0c2ce153ff1b14d101194a8aac3ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1fe7adb246521e0eb7e48cf8ae404bc23b5f9effe0c38cb3d10e947d49e5c000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226533387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efa2ab556b7b33c66e3cf9007c7581a2edba9ce4b0d661bf770025a61a053aba`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:cd606f6f489eb66f1307280aec321b3af3aa998dca447ae1cc91c6b884240064`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 53.7 MB (53739147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca8966aeb86a9f0f11248f158d2913f90028c840e94761e5f02c967158eee82`  
		Last Modified: Tue, 03 Dec 2024 03:19:31 GMT  
		Size: 103.6 MB (103633965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfb46e616beea53e8dae140de55f9bff236e6eddae30b9f5616e11f519e93e8`  
		Last Modified: Tue, 03 Dec 2024 03:19:31 GMT  
		Size: 69.2 MB (69159631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7609a4aea1eb56d952a57a226d10c8a35136bf905dab226d29cf0fc515f7ff60`  
		Last Modified: Tue, 03 Dec 2024 03:19:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1c69acd8f7d524da40bb64df3a9b993fcf9bd11da7418e4d8f9092d3c86e9438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7350479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c8afd3f8263409f211d9318b39440d1c6246599cc96378c713117e3f5791891`

```dockerfile
```

-	Layers:
	-	`sha256:ebb27afe2e8f7bd446b939793d24a40391327a7b4801e59ec090616d5162269b`  
		Last Modified: Tue, 03 Dec 2024 03:19:29 GMT  
		Size: 7.3 MB (7336237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9a2b7ad8b4a1a3c1e4d3d8a14271938a486dec4e4297aa144ef14bb417d8763`  
		Last Modified: Tue, 03 Dec 2024 03:19:28 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aae5459001181a77473e40650cf90309c6bd27f5ffa7e185e9100eeddb5d44ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.3 MB (224280352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9034230f18dd3d503a0280f1ff6a84c225942a5e1e96dc15363711d9e2e9a9e7`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e357e1f94476a03fde298261e8c007d487d3cfade45a9eef064eba724a5c5e2e`  
		Last Modified: Tue, 03 Dec 2024 01:30:26 GMT  
		Size: 52.2 MB (52245994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ddd5d354c274ecfcc46d65ee00d56e1c0ba724f5216dd62bef142f3831117a`  
		Last Modified: Tue, 03 Dec 2024 15:03:01 GMT  
		Size: 102.7 MB (102747753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e701fbe9b0a28ce175d3c6a046007f78a9ad59f3b89dc0e32297421d5837875c`  
		Last Modified: Tue, 03 Dec 2024 15:07:01 GMT  
		Size: 69.3 MB (69285960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ce4e751402750fddb6f13ce33260b940675ddb8a5639cf0aa16febbe898d12`  
		Last Modified: Tue, 03 Dec 2024 15:06:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:25f8564b04a518da1d919fcd2f01e4779f3e638e6070d45f9b93febad3a7b4e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7356399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b1347e7061c700f0460566fa11c37eed314254cead02c2f18a6841d1ae473f`

```dockerfile
```

-	Layers:
	-	`sha256:f88eca09b41793cdc4096d99383ff76ddf4387c10d00c93b6cacd91eb0a7b9e1`  
		Last Modified: Tue, 03 Dec 2024 15:06:59 GMT  
		Size: 7.3 MB (7342039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e3d50087ad648bed53d1662cc0c7f0062bddd6d765534964dada0639c9e0a22`  
		Last Modified: Tue, 03 Dec 2024 15:06:58 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json
