## `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye`

```console
$ docker pull clojure@sha256:f6405373967d2533fe3b41348c3633548e25d96e691b5e8cddcae528918fe347
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:def729b720c29291858177fa250f05c6eda10564112bf10439bb30bc04034414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 MB (230395068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de6fbeede640e2a7d2eafb4f44385a52372da5c891b0e725cb8eb53b13b877e`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
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
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a91183941977a3d5b9c6b26fa63038be9530c5c286feb444fda43596754673b`  
		Last Modified: Thu, 24 Oct 2024 01:59:17 GMT  
		Size: 103.6 MB (103634014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7530129aef98004970907c43a89707f3479e4db3ec4ae21ef38c905a8d525e55`  
		Last Modified: Thu, 24 Oct 2024 01:59:19 GMT  
		Size: 71.7 MB (71679798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b0620b596c595e88e61fbf5661bb8f6af20b532fc40b602b878366b44a52c3`  
		Last Modified: Thu, 24 Oct 2024 01:59:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:85d6bdc41229397eec7895b4a1e022deefd95a2573ce7467dfda904b34774303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7352065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25300e251ce931444db12c29d5fb54050e7a49e65537dd295a768241c3e1d8d0`

```dockerfile
```

-	Layers:
	-	`sha256:d155e2b9199cbe387254c803d630bd26b5111963bb88ff4b7b202a677a63182d`  
		Last Modified: Thu, 24 Oct 2024 01:59:14 GMT  
		Size: 7.3 MB (7338004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cf4f1f1412ad904d357551d059d6b3bc751cc39c7179188478ab7b9026cc0f1`  
		Last Modified: Thu, 24 Oct 2024 01:59:14 GMT  
		Size: 14.1 KB (14061 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye` - linux; arm64 variant v8

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

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

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
