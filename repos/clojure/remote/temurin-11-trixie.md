## `clojure:temurin-11-trixie`

```console
$ docker pull clojure@sha256:6d6e037fe1006a859b309286fc8bee310b7c87002ced6ccec73c3c8750646cde
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:8d1174f1f321d9b40bf3ddbb3a522b0493d3ef973df56c17c92719de5a7cf308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280667949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4a111347dbe47d85861ba4ed4d4ffd95e394099b68e1638841d129fff0d1fe`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:34:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:34:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:34:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:34:37 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:34:37 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:34:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:34:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:34:56 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:866771c43bf5eb77362eeeb163c0c825e194c2806d0b697028434e3b9c02f59d`  
		Last Modified: Tue, 24 Feb 2026 18:43:22 GMT  
		Size: 49.3 MB (49293124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b0e8c73eedf669e5364e653a25286cdcdf622f10f4227604deb2efa8131d0c`  
		Last Modified: Mon, 09 Mar 2026 20:35:19 GMT  
		Size: 145.8 MB (145806702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b6b388a8f94d978517fffdaf48d11b78cb7553c8642680c22184868e1819f3`  
		Last Modified: Mon, 09 Mar 2026 20:35:18 GMT  
		Size: 85.6 MB (85567477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b4be14db97d9cf8432808526882697ca443ac5459f325161b03da3888a1763`  
		Last Modified: Mon, 09 Mar 2026 20:35:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a77a00d760b02f1697e17634129b14a0310f97367d7456490ce18515244dc015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7504919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ccdcbab95ea8deacd9c3cf7781f4804946ef1fbf9a1aa080259977aaf58afc5`

```dockerfile
```

-	Layers:
	-	`sha256:28a2f537e2c65e45a91e102045a9ed5d43db228311c4462e32ee118880946395`  
		Last Modified: Mon, 09 Mar 2026 20:35:15 GMT  
		Size: 7.5 MB (7490734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f8a6549902e3fe823935cd9dac0918f06f215f3ab0436a2c3558794538ad0cc`  
		Last Modified: Mon, 09 Mar 2026 20:35:15 GMT  
		Size: 14.2 KB (14185 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2777804df82dc73c9b3df6ea8c6da641a2f264bd32c643dde9ef6ec0ba6c6b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277537158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e5092bed37139e6cf5b7da47ad1d1ec7b712f17631d5247acdf22409c2fbab`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:34:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:34:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:34:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:34:34 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:34:34 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:34:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:34:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:34:53 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ac9148dc57ca750b09f3f3da6f16324e1a3b62432b2726734535ec610e1a9232`  
		Last Modified: Tue, 24 Feb 2026 18:42:56 GMT  
		Size: 49.7 MB (49652168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75258dd608a8853bc52d4dad3936abf513e7cdf09f781c51b390a8827c6251e6`  
		Last Modified: Mon, 09 Mar 2026 20:35:13 GMT  
		Size: 142.5 MB (142501445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131d4749e09179a19e3695f793308e153f56fd0ecb38419a87bebb3e7f2bec68`  
		Last Modified: Mon, 09 Mar 2026 20:35:17 GMT  
		Size: 85.4 MB (85382898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62526466a315b7a1f5099f9b0cdff346737f613199b4cab7f6a952c68d367580`  
		Last Modified: Mon, 09 Mar 2026 20:35:13 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3c28ec7d4767db0ac2d1687d4f28c11147966a99464edb750fc2ac05a2d8ec64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7512684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1b6dcfd04b112e51931c034fa1d4e1a12d06c5e46d19a044e233e376a1a770`

```dockerfile
```

-	Layers:
	-	`sha256:9e00bb1026e6d152df17c27ed033752f27c1fb0dbaad67aadc96c4f08a9bea80`  
		Last Modified: Mon, 09 Mar 2026 20:35:13 GMT  
		Size: 7.5 MB (7498382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f985ed0660da428d880c3c2ee61a716230bbe6827bcb058628f7a55728b9744`  
		Last Modified: Mon, 09 Mar 2026 20:35:13 GMT  
		Size: 14.3 KB (14302 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:d4b68eb3c372e5590d89a4122f1d24ce7e12894f6de00a45b3cf0b4df4839071
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.1 MB (277087554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16320fd254b41173dc3cef15fb1d206fcba7728a8555009cfadb7dc9ef6390c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:48:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:48:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:48:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:48:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:48:56 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:49:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:49:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:49:53 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:468eb7cd0e9ceb9e5b1c4c9daadd36c2fd1f1ee82c667dc1a7d70fa95600a20f`  
		Last Modified: Tue, 24 Feb 2026 18:45:11 GMT  
		Size: 53.1 MB (53112261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d9812c3c8a7294cb0d2f7e16091ac0a9f181006c6d424360a6b8af498eb9d3`  
		Last Modified: Mon, 09 Mar 2026 20:50:38 GMT  
		Size: 133.0 MB (132997823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d343ec85f214f649c22e83cd7553169f67b505368dfdfde4ad5637064bdccd3`  
		Last Modified: Mon, 09 Mar 2026 20:50:37 GMT  
		Size: 91.0 MB (90976825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3a7cda731543b5896ba90787685df40f8226ba9ecd3cb56b6858b67c7e5079`  
		Last Modified: Mon, 09 Mar 2026 20:50:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b906ffa3ef032eee2e06cdd366c25ccaca4ada95881b0d929188673e38da9d39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7508772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7759b22811fb0cd6b150186a5e5f404c0d0fad76d76334d1432fcd4360250005`

```dockerfile
```

-	Layers:
	-	`sha256:95e28823dcfbfacee08eb43ed22f40d79a342034bf16755e66353e42aa473761`  
		Last Modified: Mon, 09 Mar 2026 20:50:33 GMT  
		Size: 7.5 MB (7494540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d3bba833f64e369bddf4cb5d6705af1b3da9700c4421cd8a8649e5e9fb81f69`  
		Last Modified: Mon, 09 Mar 2026 20:50:32 GMT  
		Size: 14.2 KB (14232 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:628bdb638232a82426b4218d884623f7910f83c97ac00f15c3bad029e57e9f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262447214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecfa3bf3c3416533c62f91644912c927e749f9ec2832912f405448da451d8257`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Mon, 09 Mar 2026 20:33:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:33:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:33:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:33:24 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:33:24 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:33:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:33:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:33:43 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:aba9aa950add2749194487d5c63a3069af6daf9dfe54d80cfbe32bfa7a5faa07`  
		Last Modified: Tue, 24 Feb 2026 18:43:53 GMT  
		Size: 49.4 MB (49354534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9426dc6572863c0a325dcbdc9d248dece97f4bd9dcfaf1a9a35a0a618fb8da40`  
		Last Modified: Mon, 09 Mar 2026 20:34:16 GMT  
		Size: 126.6 MB (126562061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad22ab1d74b002d476b1f1bde295e04aa249198ce5849cf19b8a42733e43250`  
		Last Modified: Mon, 09 Mar 2026 20:34:15 GMT  
		Size: 86.5 MB (86529974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202fbd2ab3d5be54905ffb183920b0b2026f1a86a55f412792f72ea01a56fe0e`  
		Last Modified: Mon, 09 Mar 2026 20:34:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1ae4a60ede9fef6439d1cf8df1700f25898f1643d4aaf5591827a7d7dbd60cf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7500844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79550fd77aa25940ac085f3ca06e4de82237e5ab943f33f9e5ab6e83552fdaf`

```dockerfile
```

-	Layers:
	-	`sha256:e2de221383aaec961857c03c9bb7f7f9eae9366d6722c63af304425d7c9e0f10`  
		Last Modified: Mon, 09 Mar 2026 20:34:13 GMT  
		Size: 7.5 MB (7486660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4cbd0cd611d67468062ee19be0f47be34a79c59bfb9812041412be13b23ec85`  
		Last Modified: Mon, 09 Mar 2026 20:34:12 GMT  
		Size: 14.2 KB (14184 bytes)  
		MIME: application/vnd.in-toto+json
