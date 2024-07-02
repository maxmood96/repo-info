## `clojure:temurin-22-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:85b85c9249e9863526aae787fd9d9ad90f7952c60249236521a3dc7fe74da7da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:4b1e9f1bf0e9765a36365fe4931f0c615728433fac135d546b33aff66c05d191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.8 MB (286782482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ec177c7e7c20294bce55bb88f9887ad3eea9e5288fa14e635a2a830f7048d9b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Tue, 28 May 2024 15:17:11 GMT
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
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ce1ed05c60bc1523b94cf36756778a0ac93ee9382ed3df1923132b7fc99757`  
		Last Modified: Tue, 02 Jul 2024 07:08:30 GMT  
		Size: 156.7 MB (156715503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99355107c2053e0dbdde81047fd54b9aaf3d4d8408793b3d38ccad26b6d4c0ad`  
		Last Modified: Tue, 02 Jul 2024 07:08:28 GMT  
		Size: 80.5 MB (80511873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eca7214f61d0cb5ecf2e8f817a6353b35bbccdc86630d6a0b1a22ddd810d6ff`  
		Last Modified: Tue, 02 Jul 2024 07:08:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4010591dc43dfad3e26041fe0acd14b43cae3039acbf7ff91554e7f5bc25b516`  
		Last Modified: Tue, 02 Jul 2024 07:08:26 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e0f1f3d615b8e68318bb90698e4df41840719882ef036d2fd586e9d1c8a50e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6976762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a6a48cb42cb9a8a28320c8226e6d1342f1187aee7d2a9badaa7ad6d29f9597a`

```dockerfile
```

-	Layers:
	-	`sha256:091346da2692377cad7d7aeb3d4f881f3d4ec6ad5e1cf77e4d651fb2c94a5164`  
		Last Modified: Tue, 02 Jul 2024 07:08:26 GMT  
		Size: 7.0 MB (6960639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f6b3b3be086a0eb248e27104d0e0729408f518391ff67b51a07c15663456e91`  
		Last Modified: Tue, 02 Jul 2024 07:08:26 GMT  
		Size: 16.1 KB (16123 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4f7259b0a2fb600e89e28713e6a11fd94170588ef8cc034c982a5a39accab5aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.6 MB (284589551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aba296e5b10db6f8a2950dc26ba54a9cbd29b106585dce5180e24a01e78df41e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Tue, 28 May 2024 15:17:11 GMT
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
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9254cd7885a46cc591cf9840aabe35758607f7cbcb4c312e42de17c9d452823`  
		Last Modified: Tue, 02 Jul 2024 09:43:32 GMT  
		Size: 154.7 MB (154737984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f719cab993bc935472d0623b365be6e2ec9314f2ed52c8f3a033f2715c95aef5`  
		Last Modified: Tue, 02 Jul 2024 09:47:44 GMT  
		Size: 80.3 MB (80262078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c63e74d0584d95006eebac5d07872e4d98107e2215364e09d5a9ef1fee33f38a`  
		Last Modified: Tue, 02 Jul 2024 09:47:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de9aff301618aac1970e3a3af271b07170b6b62d31b99974d87ecac735e1a83`  
		Last Modified: Tue, 02 Jul 2024 09:47:42 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:460bf55bd8a577602fb71ef57e96cec40f6ddcd84b35f7ef369a03ac726a3cae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6983733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8186959b6e396230607f2f4f357204f89c74d0a22d6b78e85b9afcec48b138`

```dockerfile
```

-	Layers:
	-	`sha256:f14422122cb0d0b117e3216f5257eeae14280b79227577f619feb3f86ce5fa07`  
		Last Modified: Tue, 02 Jul 2024 09:47:42 GMT  
		Size: 7.0 MB (6967050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af0afb5aeef062c5d3319118fe66be6f78d1c9f99edc71445a59d97e2e931773`  
		Last Modified: Tue, 02 Jul 2024 09:47:42 GMT  
		Size: 16.7 KB (16683 bytes)  
		MIME: application/vnd.in-toto+json
