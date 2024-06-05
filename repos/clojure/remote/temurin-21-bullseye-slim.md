## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:84114e766be9a3a2bfbc20e686705072d6d16bcf7f7efa2a5725a110a75ce01b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:714d840a1449023f58263847852af94f7f27f1fbf43b181139fff9c8dfec2d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.4 MB (248352308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc3f10dc10175ecfcee46a6e0633b2b58a24d002e6b83f6fc526fd0f3241c74`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:26 GMT
ADD file:9b38b383dd93169a663eed88edf3f2285b837257ead69dc40ab5ed1fb3f52c35 in / 
# Tue, 14 May 2024 01:28:27 GMT
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
	-	`sha256:728328ac3bde9b85225b1f0d60f5c149f5635a191f5d8eaeeb00e095d36ef9fd`  
		Last Modified: Tue, 14 May 2024 01:33:11 GMT  
		Size: 31.4 MB (31433931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7080db256fffd5c8d1202dac128df392b0494c474ac393236cdc1e6595da464`  
		Last Modified: Wed, 05 Jun 2024 06:12:30 GMT  
		Size: 158.5 MB (158497956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae729e2fd3d134d8c8f96e4578a3aee654eba4bb97d0d7ee8dd9838786ade610`  
		Last Modified: Wed, 05 Jun 2024 06:12:28 GMT  
		Size: 58.4 MB (58419377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ad38075136b5030c03e50c39558a6a4d87587dcf34f8846e8783758740965c`  
		Last Modified: Wed, 05 Jun 2024 06:12:27 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae955c8c4e15230535624fafed0937198a3d9c653f5e7f2f2c59fc0c84da8e9`  
		Last Modified: Wed, 05 Jun 2024 06:12:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:49744985092ec2acb952fe0fb8b36be1cd727a540c6bd517f16d4dea6f007fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4926098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55236ef1937ba432b84025ccc8fd0be97f4a470f63254ba8c75b21e84299d77a`

```dockerfile
```

-	Layers:
	-	`sha256:9f4bfa93ae59696a82f9330f2c9cc7f982ebd335c6758de76b561b73ffb36039`  
		Last Modified: Wed, 05 Jun 2024 06:12:28 GMT  
		Size: 4.9 MB (4909939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42ffdb852a1ae65e8efc8efeac64070ec1bc84ad6d49371c057affd841c90027`  
		Last Modified: Wed, 05 Jun 2024 06:12:27 GMT  
		Size: 16.2 KB (16159 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9459d8ff081628cb8b1ee9e284edeef7742db2e5340887d1adec85951de32add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.3 MB (245293653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:998816fee1d4efc05a407909f56214a64ac161a9ca64ec0e5aafa6daae68f1ea`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
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
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36739f47c257a5ce7926e172a2385e063cebd51a193f6f9a8289c7af2ebb3679`  
		Last Modified: Wed, 29 May 2024 21:50:36 GMT  
		Size: 156.7 MB (156665602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a60935648a3d13345349c0aa9ef19c562545d62243f63d9126700d427820e1`  
		Last Modified: Thu, 30 May 2024 00:21:40 GMT  
		Size: 58.5 MB (58540095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0976c04d468c2e0702c752f12b50c5767a2973e1a25f8722d59370a65f68696b`  
		Last Modified: Thu, 30 May 2024 00:21:38 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4567ac9aa3b629c48f89ffd309e43a868fa0ff2416c984d6a1f85759556d7285`  
		Last Modified: Thu, 30 May 2024 00:21:39 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3fbdf0aec8ece15f1fb59ac88fd86f294459cec04a162352f86040b80066031c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0192ccc8fe930747ac5326265ff44095701ea0869cdb9b304fb4769ac56c5b5a`

```dockerfile
```

-	Layers:
	-	`sha256:8a3c9ad670a9b48c6e59a983037c24fb20b14951381a724fdee3029e17c5401f`  
		Last Modified: Thu, 30 May 2024 00:21:39 GMT  
		Size: 4.9 MB (4916320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a52efc06d750e4e8720ff3cba5aa98501b08b1c350b8ad57302f1842642a680e`  
		Last Modified: Thu, 30 May 2024 00:21:38 GMT  
		Size: 16.7 KB (16724 bytes)  
		MIME: application/vnd.in-toto+json
