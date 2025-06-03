## `clojure:tools-deps-bookworm`

```console
$ docker pull clojure@sha256:03bfc18e6f662d98083bd2a5f863034ecc4f28177fac9af3a5f8a3613fb8502c
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

### `clojure:tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:cdd5d1c3ea11c73203115e4321ac092e26d5e58321d1d9bef149acf0b11b89c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287117947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f06a942fc5ab98e4edfbc558114fc3eaeed92c933dbb075b6771e1729023dbc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3e6b9d1a95114e19f12262a4e8a59ad1d1a10ca7b82108adcf0605a200294964`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 48.5 MB (48488245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa3c0578c3a59a8a3212a55463d1179d9abf668f220248eaea43297e31871e4`  
		Last Modified: Tue, 03 Jun 2025 18:41:31 GMT  
		Size: 157.6 MB (157634512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0d76532d27fbde4222b0a303a724a23739adc4146d84139dbf7755bb557431`  
		Last Modified: Tue, 03 Jun 2025 18:24:51 GMT  
		Size: 81.0 MB (80994153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9a49e1e7e3cbdebb7be7e28b92bddf3f745a9d13914c35c5c57835cee7cbe6`  
		Last Modified: Tue, 03 Jun 2025 18:24:44 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760d3363eeb087e48beff429ae3cb911572b1d364e0d6beff8bb77dc31f3b743`  
		Last Modified: Tue, 03 Jun 2025 18:24:44 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9b346cefabccddd5cc21c6f0c648c29842dd61beb3a7158da1d83550fe0855b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7241445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5d77cf8ec38c90ebf7bc3d9398882e83f3d3f0436167cfeac38fac3e9f05595`

```dockerfile
```

-	Layers:
	-	`sha256:426c2c183ae1211a412eb590d65c84372d0b93bf3a8861753bf47350db86d9a1`  
		Last Modified: Tue, 03 Jun 2025 18:38:31 GMT  
		Size: 7.2 MB (7223624 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea3d773cee9c0997302d854599a90a2d2663580f39ed135c505925e676bf9e0a`  
		Last Modified: Tue, 03 Jun 2025 18:38:32 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:54b6e99c68906b0408efd2dfc2d4f9b3e68f716696e96e3b321b330966bc92cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.1 MB (285105642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0e78a030c3e47f9dd0cac0a0fc33abe2aa9f11e4010b817b9dace0cd07ed0e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437f8f7a50b2952398084c7b3ca28b3cfe6e72e05419b0e1b568927135d80a2d`  
		Last Modified: Tue, 03 Jun 2025 13:43:18 GMT  
		Size: 155.9 MB (155928814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c560e5d0795167197d8711fb3fdd5609860a926c2347b7aa46a24f17cdd315ef`  
		Last Modified: Tue, 03 Jun 2025 18:45:33 GMT  
		Size: 80.8 MB (80848607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d1c9f6296d7e7e135beaf0aaa6c2f5af311fbd20534b3e787563e555c30ea7a`  
		Last Modified: Tue, 03 Jun 2025 18:45:23 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfbe37e07fe3a063545b738c94167ed3f63bf7d122363ad7b2d72ded50f7aa3`  
		Last Modified: Tue, 03 Jun 2025 18:45:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d5303088b4b654b450b61d8d28f2510b2ecf2668e08d3836fac0954a413062cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7247469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3465f8f5bcc64065205b1c075e5e5f454abf9127506e901e745547de6e389ae6`

```dockerfile
```

-	Layers:
	-	`sha256:58fa699733acfd5f660206746d5f6829ac11a5b9fbe5e05da225fd0cf1099cdb`  
		Last Modified: Tue, 03 Jun 2025 21:39:53 GMT  
		Size: 7.2 MB (7229459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e17c6a17fc13bcded90b84b1e6fef1555865a14c7b0e3e8c9863e12363cb7655`  
		Last Modified: Tue, 03 Jun 2025 21:39:54 GMT  
		Size: 18.0 KB (18010 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:695f007c34b8f260cc9a213e202469bc30a3370d62f68aba40eb356e64f689cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (296950953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86ace4fadda323204d46b9035f7714a867d7752efa775fc5262a120dbe2ffec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860dcfb7182a5dc32b212ca727ac1ab0a7e7f5698fd7540ceb4c7f84c97337da`  
		Last Modified: Tue, 03 Jun 2025 08:01:20 GMT  
		Size: 157.8 MB (157804869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748c45bc94716324b93adfa35563c87437f83790c9711b5ce1cdb52a4dfadd03`  
		Last Modified: Tue, 03 Jun 2025 18:59:55 GMT  
		Size: 86.8 MB (86813423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f45f62ed1a1450f3b5ce10a89a1195170174ab07a66f7fb005a2d42099e655dd`  
		Last Modified: Tue, 03 Jun 2025 18:59:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda43b5d187d83f114fe541b12941e69c5c036d35c11316ff9fd6d2618289c32`  
		Last Modified: Tue, 03 Jun 2025 18:59:48 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:442ed7ea10df77827eae706c2d70faba4adc1190af99c14718f1b9b3e83db6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7246769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ea6091a6b3ce426337eb37c4036dabfdac4edc8c72b3d206a550d6dfa1af24`

```dockerfile
```

-	Layers:
	-	`sha256:810750634ae7b0875bf6b93f48bec9a6dd9adfd4efce9d2f5bfb6b59fe4f3ae6`  
		Last Modified: Tue, 03 Jun 2025 21:40:00 GMT  
		Size: 7.2 MB (7228864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c84b28e5b3707c6d3801cee4fe1059c7320e75e18b11cda1fb2df0bedc267de`  
		Last Modified: Tue, 03 Jun 2025 21:40:01 GMT  
		Size: 17.9 KB (17905 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:8a076bd6fec83b9f37342be9c385b6503401fcd79bbcacbd767458e2c68a27a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.9 MB (273858683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8755e5ae905afb4f5b44d68109dde87ed86bf25fb97690a06048b6fa74e6756d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:47f9a2c2279c9df9e222a4c8af501e43b0b5e2552eda9597a97162080b8f106b`  
		Last Modified: Tue, 03 Jun 2025 13:33:39 GMT  
		Size: 47.1 MB (47143842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0351b5becfe334f70decb5f4368fae95fc08263ea48dd42b0157f6c4565135db`  
		Last Modified: Tue, 03 Jun 2025 05:59:18 GMT  
		Size: 146.9 MB (146911002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b60927529637d4c1c92970a20c8eb5feb956f702ffed3ca56bec6c38560c1a`  
		Last Modified: Tue, 03 Jun 2025 18:37:57 GMT  
		Size: 79.8 MB (79802799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e6f8c78ef3477b13b8832e6bfaf7c872d7cc4459558d4587f871ec45db4629`  
		Last Modified: Tue, 03 Jun 2025 18:37:40 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7b2da7cb5240f99ca675aaddfbbb6dc4b026d114de0e5fcf2da5ed96f152bc6`  
		Last Modified: Tue, 03 Jun 2025 18:37:41 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4f525364ba4edf7900f04d727fc915829ba6d429aebe6a916d45f00fbf095c5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7235656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f931da4c820b4cbd4f9b130802397e23634835602e8038614e60c2aaf56dd9b0`

```dockerfile
```

-	Layers:
	-	`sha256:433077378defb0ac6ee55b7ea4022d312f4e1878fc4093206481e89462a0e420`  
		Last Modified: Tue, 03 Jun 2025 21:40:08 GMT  
		Size: 7.2 MB (7217835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3e0738bb4688949d2530f7b21f1c3074dd319b063266439fcf000e4074be3cd`  
		Last Modified: Tue, 03 Jun 2025 21:40:09 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json
