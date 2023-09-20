## `clojure:temurin-17-boot-2.8.3-bullseye-slim`

```console
$ docker pull clojure@sha256:b368afe8326ad3d3b277f1c120194cef1d009ac381d7637191e186eb63e1e632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:eb97933742e1eb6df562551f7b7f8d54e8eb7fda7cbbe2942b99d8aab3b8392a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236091720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d7e40f1dd7b9da21450a268da824797fc95bc1f9d295d8a160407fc98f62bdc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:22:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 Sep 2023 07:28:19 GMT
COPY dir:61bbef45bd137d5078f6a6f774d9bc49d275ae5fe27274294232d075ae1a5bf2 in /opt/java/openjdk 
# Wed, 20 Sep 2023 07:28:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 07:28:20 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 20 Sep 2023 07:28:20 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 20 Sep 2023 07:28:20 GMT
WORKDIR /tmp
# Wed, 20 Sep 2023 07:28:26 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 20 Sep 2023 07:28:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 20 Sep 2023 07:28:26 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 20 Sep 2023 07:28:44 GMT
RUN boot
# Wed, 20 Sep 2023 07:28:44 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 20 Sep 2023 07:28:44 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 Sep 2023 07:28:44 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f849626c60449d70414a79d12d1df3b48aa0c9fe4ae3176ba320531d57b9d3`  
		Last Modified: Wed, 20 Sep 2023 07:37:37 GMT  
		Size: 144.8 MB (144775758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19c1e8c3a86b82cfaa807035a7a968e324b909729bb3b23575fc38e4372ed12`  
		Last Modified: Wed, 20 Sep 2023 07:37:26 GMT  
		Size: 1.1 MB (1077548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b38adf28b3f10eb3c89043d2d3f738395d27ae1d9fd03b850cf47ab79b29f7`  
		Last Modified: Wed, 20 Sep 2023 07:37:29 GMT  
		Size: 58.8 MB (58820305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1397fcda0b074f0b2fa26444da57a521dcce35d60618e57762217daac493af70`  
		Last Modified: Wed, 20 Sep 2023 07:37:25 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:73f986b49fe0f1a73db22fd972c8a9c0aa38c788a4ad842af1fbfac6c221740a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.5 MB (233491962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88104b988afd7753245a0d8b96959f4df8841ecf1f6a5d1a136cc6a6916f50f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 07 Sep 2023 00:39:53 GMT
ADD file:abd1ad48ae3ebec7a6ecc8ce3016c25be2afcbaedfcb904bc89b1ce59400aef0 in / 
# Thu, 07 Sep 2023 00:39:54 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 06:46:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 06:46:35 GMT
COPY dir:ffc7dc4725a3524e0b294e59a90d1e58e69ec448374b50aef6bef0cfa219cb0f in /opt/java/openjdk 
# Thu, 07 Sep 2023 09:09:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 09:09:46 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 07 Sep 2023 09:09:46 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 07 Sep 2023 09:09:46 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 09:09:51 GMT
RUN apt-get update && apt-get install -y wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 07 Sep 2023 09:09:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 07 Sep 2023 09:09:51 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 07 Sep 2023 09:10:08 GMT
RUN boot
# Thu, 07 Sep 2023 09:10:08 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 07 Sep 2023 09:10:08 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 07 Sep 2023 09:10:09 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:f96ab15157043879c2ff23e0556e798eba6a6ff3d7fd5d1384de223bb9f66f1d`  
		Last Modified: Thu, 07 Sep 2023 00:43:41 GMT  
		Size: 30.1 MB (30062903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0067a4775f017792de5f753490d0b5645640bc00f5c264295100a66ea689ec96`  
		Last Modified: Thu, 07 Sep 2023 06:48:31 GMT  
		Size: 143.5 MB (143543493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a7431cdebb714dca289c54cad5e769b95466db8459a203840468ac78b6ce765`  
		Last Modified: Thu, 07 Sep 2023 09:17:42 GMT  
		Size: 1.1 MB (1064800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9afe617e30ae4f2eae6d83874b104e309baf51a13ab1cdcb4e0f4b2ff1fdb2e2`  
		Last Modified: Thu, 07 Sep 2023 09:17:45 GMT  
		Size: 58.8 MB (58820367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4a6ad8813cd8d68061045262559bfcb7c32943f714eb926ea624957df25298`  
		Last Modified: Thu, 07 Sep 2023 09:17:42 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
