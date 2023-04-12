## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:547e372f3e581bb079197370eaa1cd1679d3ebae9e3c19dc9ab31944e19386a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9e49d3648b6006d9d3079429b8cff413f12ebd45f8a900807926c72e1c084f80
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.7 MB (308666390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b800d0c505b18061a282399b5ce6021c0740e264f9544a5bcdf4e6cc60d5544`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:15 GMT
ADD file:459d1e92eb8c24ff4758f974d289ca8a2abe04cf50b6fe2bd760aa4589478289 in / 
# Thu, 23 Mar 2023 01:30:15 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:16:58 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 23 Mar 2023 06:22:38 GMT
COPY dir:d90c8d6564183f8aad11f93ecfb2f7e0eeff18588ff2b62d7ca3d8d30672bc2c in /opt/java/openjdk 
# Thu, 23 Mar 2023 06:22:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Mar 2023 06:22:40 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 23 Mar 2023 06:22:40 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 23 Mar 2023 06:22:40 GMT
WORKDIR /tmp
# Thu, 23 Mar 2023 06:22:46 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 23 Mar 2023 06:22:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 23 Mar 2023 06:22:46 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 23 Mar 2023 06:23:03 GMT
RUN boot
# Thu, 23 Mar 2023 06:23:03 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 23 Mar 2023 06:23:03 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 23 Mar 2023 06:23:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:3e440a7045683e27f8e2fa04000e0e078d8dfac0c971358ae0f8c65c13321c8e`  
		Last Modified: Thu, 23 Mar 2023 01:34:00 GMT  
		Size: 55.0 MB (55045608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:803b6efe2710f8afbae0603df0d04f44f97f99a0a0a87709cad6c690fb01572d`  
		Last Modified: Thu, 23 Mar 2023 06:32:29 GMT  
		Size: 192.4 MB (192438264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3cf0ff3bdfe63d9c3313e7d2fc8488205c6d76ba227d9d0264b4e75faa7d6c3`  
		Last Modified: Thu, 23 Mar 2023 06:32:16 GMT  
		Size: 2.4 MB (2361571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973bc8e6b4e4175ca9c33f6038aedccf10f3733f298bd8df5ce444eb48ac8668`  
		Last Modified: Thu, 23 Mar 2023 06:32:19 GMT  
		Size: 58.8 MB (58820548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6d85b76a7acf0f226438b4e46ae8d43e1023213861a7a971198a16d593130e6`  
		Last Modified: Thu, 23 Mar 2023 06:32:15 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d61d9fa4e3e0a11162c70c85914867a441b40bd1ec6a92e3ffc1cb00e0b4a9ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306137935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b64944f09128f18d8722edd3e4e46d367c7ed0e3024ebfb584b613c883395ac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:42 GMT
ADD file:dd3d4e5fe819950e7d01b44a29dbd790438cd722ba76198910e2597448ab0c6f in / 
# Wed, 12 Apr 2023 00:39:43 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:18:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 12 Apr 2023 01:23:04 GMT
COPY dir:44544f5117ae50af040f98b1979efcc18f4c9f0c7257bfc4a37b80697337361a in /opt/java/openjdk 
# Wed, 12 Apr 2023 01:23:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 12 Apr 2023 01:23:09 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 12 Apr 2023 01:23:09 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 12 Apr 2023 01:23:09 GMT
WORKDIR /tmp
# Wed, 12 Apr 2023 01:23:14 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 12 Apr 2023 01:23:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 12 Apr 2023 01:23:14 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 12 Apr 2023 01:23:31 GMT
RUN boot
# Wed, 12 Apr 2023 01:23:32 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 12 Apr 2023 01:23:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 12 Apr 2023 01:23:32 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:dc80b8cdbfd36cb20231d807a50d704945d1df4da8f6e23197ccfcb629970491`  
		Last Modified: Wed, 12 Apr 2023 00:42:14 GMT  
		Size: 53.7 MB (53705529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6911e57ac771aafcbe41270c1285de884dc5ce0d79a1b3069ec89c3a65e4a6c2`  
		Last Modified: Wed, 12 Apr 2023 01:30:58 GMT  
		Size: 191.3 MB (191260417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50295ccbef2d622619d71394f82358bc9fa77444c9a752eeab3cfb6283a724f4`  
		Last Modified: Wed, 12 Apr 2023 01:30:47 GMT  
		Size: 2.4 MB (2351068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e1b4e3499b217c6da14be39e1d22b620ddd35f56661eabaa0cfc1dd777f5c0`  
		Last Modified: Wed, 12 Apr 2023 01:30:50 GMT  
		Size: 58.8 MB (58820521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0424e97b38c6dc6198ec2a0d6311298be19bc24147a9b04869280659081fe24f`  
		Last Modified: Wed, 12 Apr 2023 01:30:47 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
