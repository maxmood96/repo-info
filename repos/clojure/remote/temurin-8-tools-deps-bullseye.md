## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:34637d87ec8b8cceedde8484be8c05700590776cee4900bc5ae7b4c9903ddd17
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1994d75a2920ebb4616d14c14050af675dc11b7e69d27dbb7c339b5a853175ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227881683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc6f665a93b954a2e4362d22efe857dde029d57a62b0e3127205fb8b9427668d`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:c2056d933cd629f55ac55802dda223f122286bf60ec42a24f0d0f6ae2615315c`  
		Last Modified: Tue, 12 Nov 2024 00:55:16 GMT  
		Size: 55.1 MB (55108780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d890f17d44f93043a29704338d04041f083f1ad2898ce42520ff03d9220e38b`  
		Last Modified: Tue, 12 Nov 2024 02:22:51 GMT  
		Size: 103.6 MB (103633891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a69af698628b57756636d2bbe655e1b4e873a8862cfffc820a2fb33e8dd932b`  
		Last Modified: Tue, 12 Nov 2024 02:22:50 GMT  
		Size: 69.1 MB (69138368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c2fd81349f9ded29ff2bfe2b4edc46b4d70b882016e404cbe9aa715c4e8b73`  
		Last Modified: Tue, 12 Nov 2024 02:22:49 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c489f94fc0b0eea287a7de84a03bed8318dcc8e65165d045015683d7e74bb2ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7352281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b8046819bad2d99a2b6dd8be332cee4c1999452d150becee246048f872faa99`

```dockerfile
```

-	Layers:
	-	`sha256:65548163013a6982ba1cf20b5b1432d282cd57232b2902ee83b5f8e4c2598146`  
		Last Modified: Tue, 12 Nov 2024 02:22:50 GMT  
		Size: 7.3 MB (7338040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:504c2423cae46804973a1f103fbda3ec9a7bd0223943ade8ec75544db762519e`  
		Last Modified: Tue, 12 Nov 2024 02:22:49 GMT  
		Size: 14.2 KB (14241 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a82962542b7aab069ef3a73a391616449e7848fa0e4a3be8b09407d73980bd66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228254965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9918a3d12a31156d166063841c0e260ea947546fd7b56b100efe7a86eeeabea6`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
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
CMD ["clj"]
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777bc65e0cc7a80302eaf35012cae747c2f19cb6b0886892108cb66f0ed6ef49`  
		Last Modified: Thu, 24 Oct 2024 08:53:38 GMT  
		Size: 102.7 MB (102747729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9868ab6c9f9876e668c9dd686781ddd43bfa16d930d8f1b761ac5fcec8bae7ea`  
		Last Modified: Thu, 24 Oct 2024 08:59:35 GMT  
		Size: 71.8 MB (71771697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6de8f70180d7a4dfabd56475eee752c695994c5fa164f13266261177f7e27b`  
		Last Modified: Thu, 24 Oct 2024 08:59:32 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1be201f0c1e54e36acfc12ad181a32d1b1835ed6fe1c0051fb2a4a9aa5669a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7357979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b4d447071306e0b6376b76a5c1d4063429f193b3a10b4bbc90669d6c527f37`

```dockerfile
```

-	Layers:
	-	`sha256:fb5b8ae6e0a401666866e2dfea1c2931802e079cd600f6f5f3a05cfacc148a1c`  
		Last Modified: Thu, 24 Oct 2024 08:59:33 GMT  
		Size: 7.3 MB (7343806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8a253dc03c0c079d20abe3ef95c6b2dd0e0658922eab7eb27c8aedc67b759e0`  
		Last Modified: Thu, 24 Oct 2024 08:59:32 GMT  
		Size: 14.2 KB (14173 bytes)  
		MIME: application/vnd.in-toto+json
