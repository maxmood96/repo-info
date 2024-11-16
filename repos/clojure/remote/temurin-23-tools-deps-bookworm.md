## `clojure:temurin-23-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:e183d341bce342c7cb3f216dd29b36fa964af87e6ea6415643799ab0e5a622ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:4346029523480adf7dbf87da7193f0af6b9689173594b9c15af49459e79bd293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.8 MB (295809844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05262bb213082c89e4a56ba9c5ec96e6bbc276331e02af197656e19687d66e4f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b2b31b28ee3c96e96195c754f8679f690db4b18e475682d716122016ef056f39`  
		Last Modified: Tue, 12 Nov 2024 00:55:23 GMT  
		Size: 49.6 MB (49575695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c2e95299ef9c65591b3df8e50ec587666fa5c7b4ffa7bb453db141cb007a37`  
		Last Modified: Sat, 16 Nov 2024 03:51:47 GMT  
		Size: 165.3 MB (165295082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2086029a4e1fd3e4399b3b0a9adcd6971924dc0c659ddce749ed23bf7665231`  
		Last Modified: Sat, 16 Nov 2024 03:51:46 GMT  
		Size: 80.9 MB (80938028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d748cc4a19e3ceaa5690177ada06914f1d166d66036d389c6df75ff2256318f`  
		Last Modified: Sat, 16 Nov 2024 03:51:45 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bb925c77c1a55db642c8aedd8a825a504ef946d97d170656ab137772c7c579`  
		Last Modified: Sat, 16 Nov 2024 03:51:45 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4e217d4ad10a7ce77a4bdd04cc03bc4df9b084b2e7c475b8a17af08f547f482c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7204624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2d7e4943b075bec211bd9a6e5b68f40bf2d239a6b751ed5e4aacc0cdc016ae`

```dockerfile
```

-	Layers:
	-	`sha256:12bb51079008e780d52f7579b954abbf9108c51295b44c7802d9bf81c3f8f684`  
		Last Modified: Sat, 16 Nov 2024 03:51:45 GMT  
		Size: 7.2 MB (7188120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59e5cd467fb0f0963ccd1f82b06d69f96ceda93196f487da4ed42518023bfcb3`  
		Last Modified: Sat, 16 Nov 2024 03:51:45 GMT  
		Size: 16.5 KB (16504 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f41b0f970c1e2991b0b18e632af5c73460af6ba0ebaa3c87c1bf7f95c4405653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293668060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:529ec133ed6eb44577dabe31c0daa311d0b2a35fd2e2ee2991bc82da4c33035c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39deae920147b40fe519b6d41ef8d1aa18333b66459594eed15473c7794b25ae`  
		Last Modified: Sat, 16 Nov 2024 05:46:37 GMT  
		Size: 163.3 MB (163281799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8731c564e79d437d930119be5db7c921a197260de4b14d9b1d39743fc949c7`  
		Last Modified: Sat, 16 Nov 2024 05:51:41 GMT  
		Size: 80.8 MB (80798022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378f11bc97552923b07c695c910f21f8db136562904ed9a3e0964384713f190b`  
		Last Modified: Sat, 16 Nov 2024 05:51:38 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455a56b03ee0659c5120a4abc6bf494e604a6b4103dcffbc903297fa7399feb6`  
		Last Modified: Sat, 16 Nov 2024 05:51:38 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d79cf9a4034218bc333ab66df58fca9f90bee74c4ac8906bf4c4237c95c95f5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7209936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e523dd442cd38052b124ff3d5d5fd2008fea8fd266ca19ee7e02507f0f7a28e`

```dockerfile
```

-	Layers:
	-	`sha256:a6521166a761cd35ed562e0a966233e2769b32f0ee901fec1a92361776b24933`  
		Last Modified: Sat, 16 Nov 2024 05:51:38 GMT  
		Size: 7.2 MB (7193290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ef02329080a1131529385a2a972e7e183bf1b371b49edb989b62acf3ea68d04`  
		Last Modified: Sat, 16 Nov 2024 05:51:38 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json
