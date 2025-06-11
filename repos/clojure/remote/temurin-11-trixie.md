## `clojure:temurin-11-trixie`

```console
$ docker pull clojure@sha256:27a3b4ca241b64446a5ddd8c49f856e1891604466c18ff7c4c94a016de14b601
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
$ docker pull clojure@sha256:f1e6c03a2dd78fa85b84412e487fa042d9ab71fe0c10ea698140df9432160745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.2 MB (280155432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1c29bd4efa8a18aefefebcc452933fe48f79564e3430b3220c29324e131add`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d8e51f6b7dcdaee60f07f9a13a971abe1be9dc977d52d0849087118f80a1c7d6`  
		Last Modified: Tue, 10 Jun 2025 23:25:45 GMT  
		Size: 49.3 MB (49253859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e276e48228457a29aed7d098606796a5020b4a6bd5e45d8c3f3d6c9141c72200`  
		Last Modified: Wed, 11 Jun 2025 04:21:01 GMT  
		Size: 145.6 MB (145635595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe7cfe902916b644abd3a61747f41ecc81aba901e8b00df009a14201ca8feb0`  
		Last Modified: Wed, 11 Jun 2025 00:13:51 GMT  
		Size: 85.3 MB (85265331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339e2f387b7c18657a1f4a2af9153a0c219c0d8e078c1b434af103d2f4feee19`  
		Last Modified: Wed, 11 Jun 2025 00:13:46 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:77d583c8565f6942592c3f069b22786f7c1dde99ed644103277cd57ba5378efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5653e398a9d12a42f27ba4a67ff816532597e67df2494ba53c54b660857982a`

```dockerfile
```

-	Layers:
	-	`sha256:20c17e8c5a6199fd27b715b1ba47044cd20a4c7839af5ae98f45ac8c2616bede`  
		Last Modified: Wed, 11 Jun 2025 03:36:12 GMT  
		Size: 7.5 MB (7479290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36b6cec5be3b3f9e8394746080d215fa0f6478ef848e32b4bbd84d762279d6a1`  
		Last Modified: Wed, 11 Jun 2025 03:36:13 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:980df3795b0606605841b14b8c99e1868af409140c313078af8825fbf3b21142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.2 MB (277239175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a2bed20d16f4e53f95ff36b3bff08f31f2bc5e1aabda8264005ee4f53803647`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:546a427a0109bbde3a869c6a4ff1ed90ec74768e7fd82dd00441608d83416632`  
		Last Modified: Tue, 10 Jun 2025 22:52:49 GMT  
		Size: 49.6 MB (49621528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d780a3a01a9b1dea561cdbd6b3757dc17dc751380a900c5d002fde515f87636a`  
		Last Modified: Wed, 11 Jun 2025 08:17:29 GMT  
		Size: 142.4 MB (142420640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ea44cec7b0de0184833dae722c0cfd35fc21fdde0b1256cb45e59984a4485c`  
		Last Modified: Wed, 11 Jun 2025 08:22:21 GMT  
		Size: 85.2 MB (85196362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df23f82ce32a4db6347b9eb25a3d22d1965bbdbec4e07f7cb9a20889d27e092`  
		Last Modified: Wed, 11 Jun 2025 08:22:19 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ad5484085b1aafaf2f6d6d427e893107181c94301f41c92adc0bf0c16c316335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7501284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac72a510ce2109ca1be9d1d67b8c322d42affd177af6827c4525e68f1b6daea0`

```dockerfile
```

-	Layers:
	-	`sha256:f7df23b2268603593c65f68aaa7162b67ec18b86fadeb219064ea807a2ef0e2d`  
		Last Modified: Wed, 11 Jun 2025 09:36:51 GMT  
		Size: 7.5 MB (7486938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:628da8d79d826bd00ddf3df144a29d32fe5162d05115a1b9d29f81a511d2b1ce`  
		Last Modified: Wed, 11 Jun 2025 09:36:52 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:48179c0f23d7ef53b666000a72113e16eaa35fd81d6e372607bb3d779ed2898a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.7 MB (276674228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7bd1ca7a6eadda594c73d1d26fd7ff3e8da8260c94fe1c594b608a61bfd3c0`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:70a0e6b9f26ae2a311f0c79d7ff095922eec7e2aa39f94bd8c4e5b385cfa847d`  
		Last Modified: Tue, 10 Jun 2025 22:52:26 GMT  
		Size: 53.1 MB (53090933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49286209f3e7a5be1dd9c3b24940b38ada681e5c4f93cc34c9d73f2a033fc2e9`  
		Last Modified: Wed, 11 Jun 2025 08:16:39 GMT  
		Size: 132.8 MB (132810531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46a79af906f647f3b2b84a3fbe6367cfa1bbc2c30628426565832cbba0690938`  
		Last Modified: Wed, 11 Jun 2025 08:22:41 GMT  
		Size: 90.8 MB (90772120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc556b3cbde8fc8f7ba03b47d33ee74f64cb9d09bda3ece39804d98a78a7bb7c`  
		Last Modified: Wed, 11 Jun 2025 08:22:38 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2aa749f8f9dc28cc7bd47a379dc7cb8bdd0f260ed23064f2648ce63fb196ad69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7497368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5d9790b088b5335da81153d305028e843f257f15a8c040483af45a0772ac75d`

```dockerfile
```

-	Layers:
	-	`sha256:9bc3d15e6dd761a84b8faaea31e234caffdf9706919cbcd852bdc72d17d0dcf6`  
		Last Modified: Wed, 11 Jun 2025 09:37:08 GMT  
		Size: 7.5 MB (7483092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59d640ffc81301c6e600f163eb122a9c5523901f5eab4f60ebb675f31f548e0c`  
		Last Modified: Wed, 11 Jun 2025 09:37:09 GMT  
		Size: 14.3 KB (14276 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:78f99ec00e486adb28174441fd6142a75befb765b67fd2fdeb22bd48859e5d27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.3 MB (261263488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba90a9ccb860bf31a6b6172534d40d659b9e9de738c5bbbd40ee396a12cb0682`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1ffa7429d410cb8e2162450d6c2fc3a21121304db16d73a6b9feaa05000dde5c`  
		Last Modified: Tue, 10 Jun 2025 22:53:14 GMT  
		Size: 49.3 MB (49329768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd6944b69ba7e7281759a5cc5e35a5bae4d17335c68d113e716d6f2602cb231`  
		Last Modified: Wed, 11 Jun 2025 05:35:51 GMT  
		Size: 125.6 MB (125585329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a996cd4df2c4c38f77e7d1ac9bac4ffb4121aef5d99db14a24876a38716b4535`  
		Last Modified: Wed, 11 Jun 2025 05:39:30 GMT  
		Size: 86.3 MB (86347747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf941be2defeec5352f1d9bbfa588f06d5aeb1558f9e9db4853ec9718b2f5b1`  
		Last Modified: Wed, 11 Jun 2025 05:39:29 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:1b7d6896cd12ae6e2bd42e81cc78c6e49adea46ba812f45a267152ce25f480a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7489444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:327c1238256c3feb56df582b840d3fdafef110c7b12b0a50c48eae4b6b2339b5`

```dockerfile
```

-	Layers:
	-	`sha256:610aa7bb85bb357917d13c9552e7b0ded2b17276a7eb73a1dea4efaa1d97c499`  
		Last Modified: Wed, 11 Jun 2025 06:36:01 GMT  
		Size: 7.5 MB (7475216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bdb8bbb1bcb2da08d3aba0663ff1f168e81cfcc19961f13bc792b25dd9c38ba`  
		Last Modified: Wed, 11 Jun 2025 06:36:02 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json
