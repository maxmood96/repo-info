## `clojure:tools-deps-1.11.3.1456`

```console
$ docker pull clojure@sha256:808d730992e7d0fa6203b5dbaaaf33bd955912df5867417d40eaa7d40d9fa532
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.11.3.1456` - linux; amd64

```console
$ docker pull clojure@sha256:24d567f0588063dc7bf8ff1472936a40803b71ffdd1a714797579a6781d01cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288374120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cef637ec94e2a5dc060d8dfdf66daa85872429c8a36f9b2c4faab3c532f4e02`
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
	-	`sha256:ad246211a32d46848be9601189d9208d315885aedbe572a849a9c4f66e28a555`  
		Last Modified: Wed, 05 Jun 2024 06:10:32 GMT  
		Size: 158.5 MB (158497970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55d1f2a4fe702ec4da105ca3d2ecc8506cbe8d17e232f407c66b58deb693bc7`  
		Last Modified: Wed, 05 Jun 2024 06:10:31 GMT  
		Size: 80.3 MB (80298717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc8f69844e4d9c9006da1bc4faa60b9ced5b5fbcd4ed048deb78e956816c2a4`  
		Last Modified: Wed, 05 Jun 2024 06:10:29 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb947bda822c6494016a0bbc48473c4010154cdc047178df10a8660b512ba31a`  
		Last Modified: Wed, 05 Jun 2024 06:10:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.11.3.1456` - unknown; unknown

```console
$ docker pull clojure@sha256:7fb8fbd04339319c463192332d497d344c62ef038172b6745c0a2cecaf8ae60e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6980066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817a75155f6adbf140844a16cd345edd6f389fb91890e28f5eb4ffb1dc097e55`

```dockerfile
```

-	Layers:
	-	`sha256:2633d806ea5df3fa497eab6d4fd99bbda5f3c509a766364b1b225034f21ba5ff`  
		Last Modified: Wed, 05 Jun 2024 06:10:29 GMT  
		Size: 7.0 MB (6962676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f84ac94ccd3f8aff6c572d02fdaf305b90ba7b2b9d11716bc32e950cb40d3b8`  
		Last Modified: Wed, 05 Jun 2024 06:10:29 GMT  
		Size: 17.4 KB (17390 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.11.3.1456` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:19e2c2f7c827aa799f7f3f883f5556d2adade868d5b93bdfb4f601143c475b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.3 MB (286325087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3d76eaadf46d82647ca1a47519c181dca3f5e33b63e6e1df88ec2307145cff`
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
	-	`sha256:5f8cf129a6a2c7c80a986dd2af0048d3bb592294757df25be757b347870821dd`  
		Last Modified: Wed, 29 May 2024 20:23:00 GMT  
		Size: 156.7 MB (156665610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170b17dcdeadde8a34733c4295ca704bcb78b3c801d6377e552c9648c98b89e4`  
		Last Modified: Wed, 29 May 2024 23:11:01 GMT  
		Size: 80.0 MB (80045041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59cd1ffd0d0c27a432fbbecb38956c5636c3226ba0af6a8e25beb560c3bdc18`  
		Last Modified: Wed, 29 May 2024 23:10:59 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dee76091eb9397daa40d2818c3c108b22fc8aa7ae911fed306e19f5598c6e3`  
		Last Modified: Wed, 29 May 2024 23:10:59 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.11.3.1456` - unknown; unknown

```console
$ docker pull clojure@sha256:f079d39208b2b488283dd824333b1d3b2846e6540a5cb7520190af50663bc8a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6987134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7d3c6bdbfa6eb2a921e50fd881c6bbbd97450cd03b28e9786a07511ac54fc7d`

```dockerfile
```

-	Layers:
	-	`sha256:806f8dc099dbb8f66d1448f6e8d5f660b2ddddedbc294127f4b02934969a018f`  
		Last Modified: Wed, 29 May 2024 23:10:59 GMT  
		Size: 7.0 MB (6969136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a42af80b09aa1d171ea63c29a8adbb98987d36cec8332739dc640ccd6af9c15d`  
		Last Modified: Wed, 29 May 2024 23:10:58 GMT  
		Size: 18.0 KB (17998 bytes)  
		MIME: application/vnd.in-toto+json
