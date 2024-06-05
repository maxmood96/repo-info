## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:bdb5341d3c421d0ed298f5e117326180b11e94823dea8032a8b9eadb3df2e2b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:45e260d4b4fb7f9088be68e37432ddf2eda78d6d65e1efe12cab9406bc5c4a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.0 MB (274971894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9968f05900d7fa3203d03581b3c53779166e13d6395d94d6dc4427c57e3a45`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:27:51 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Tue, 14 May 2024 01:27:51 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0456ca8fcacbb5f58fbe1d2e372e7b8ae6f2951197eeeca68d69222522f83201`  
		Last Modified: Wed, 05 Jun 2024 06:10:18 GMT  
		Size: 145.1 MB (145095091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9869d9d6f52562f236b27c4b0c74f7038b3ff1eec6dcee4cf1a90c24e751ea62`  
		Last Modified: Wed, 05 Jun 2024 06:10:17 GMT  
		Size: 80.3 MB (80299366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d3d53d4406c80d9df6a2ff64fabc290c57d0617b3d0664bcb7a307b9f29fdc`  
		Last Modified: Wed, 05 Jun 2024 06:10:15 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51baec31d4e3245dce59421d41f9e84ab35383cbb1cd9eda3d6900cc80dca045`  
		Last Modified: Wed, 05 Jun 2024 06:10:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d3d7bba1972066ee93b4e8de72838ae66a1286c62f5b57ee8b2349e25f343a9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6976056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4be8448ae55071700a68e4717d39a64c1eaa040b825bd2d017b46b1e6ce5e37e`

```dockerfile
```

-	Layers:
	-	`sha256:ff18e49c536bb8ff69d8e1630062fabed5ec8a6e13638fa45ed6be37b9e6aee0`  
		Last Modified: Wed, 05 Jun 2024 06:10:16 GMT  
		Size: 7.0 MB (6960666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83fc9033db847a3a97f9cbe7724179e2df374b46ab433c79beb6f9e0bd547616`  
		Last Modified: Wed, 05 Jun 2024 06:10:15 GMT  
		Size: 15.4 KB (15390 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f86b7732e588bfe3312f7b5c39ab8847004ce9afbce002047c3d4556faa122a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.6 MB (273552139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e878d196734fcd995ff83032c1f5076c2c892335505d15e4a5fc7661b5e46886`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:32 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Tue, 14 May 2024 00:39:33 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119c384e4745e06bac611ffc89d508c16591135572c2404a072d77b5f04056cb`  
		Last Modified: Wed, 05 Jun 2024 14:02:40 GMT  
		Size: 143.9 MB (143892779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d183bf6bdbbd05e8aa319db29123750d3ecd1c139abe99bdf3d88f05f563f3e5`  
		Last Modified: Wed, 05 Jun 2024 14:07:32 GMT  
		Size: 80.0 MB (80044924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08c17406957d0a53ec937ce3b664ef8141eed6d2c29aadcdb378900f021624e`  
		Last Modified: Wed, 05 Jun 2024 14:07:27 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9c1619a15442304576f6efadfbd5814659c23d0624803ac28a1b48f1a1886e`  
		Last Modified: Wed, 05 Jun 2024 14:07:27 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:68499c7577b71182fa33e6d57eec1df0244ca48ac85d3ccd5b1fc30d17467dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6982978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a31eccd4d28960181c0945cb8daecf3519efc950e13fd373917776487ffef9fb`

```dockerfile
```

-	Layers:
	-	`sha256:3bb7d7953ae7433b105016f481e2f8343a6f702725e360f8f82667cdb5a7a710`  
		Last Modified: Wed, 05 Jun 2024 14:07:27 GMT  
		Size: 7.0 MB (6967053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:773ce9473f964c6afd28210aafd57c11f07d9be7c6ec01c1cb5a26ef6d65512b`  
		Last Modified: Wed, 05 Jun 2024 14:07:27 GMT  
		Size: 15.9 KB (15925 bytes)  
		MIME: application/vnd.in-toto+json
