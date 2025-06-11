## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:270d679f1e0a30209fa60217b7692bd6aa939da7a50d1664de28151df213835e
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

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:e60db1ed198b4997fdfe52d1d6f6512f35670050cfa4ee95f3ef5bfeecae17dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.1 MB (275124201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33039fcc87bad146fc5fc55a2f737567d8c6e05ac99f8a265bfebf356ab2d213`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:0c01110621e0ec1eded421406c9f117f7ae5486c8f7b0a0d1a37cc7bc9317226`  
		Last Modified: Tue, 10 Jun 2025 22:46:22 GMT  
		Size: 48.5 MB (48494272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da06df41289576e340997e2b274889771fde6687bf3db1524841f3350465953`  
		Last Modified: Wed, 11 Jun 2025 04:27:14 GMT  
		Size: 145.6 MB (145635655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4349da6b28f18006b38b560a08d3ccf7520e95a93722309c5d6c54ffd221ab50`  
		Last Modified: Tue, 10 Jun 2025 23:51:20 GMT  
		Size: 81.0 MB (80993628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bc291e7fcadf08ae3b2b90f327fc3cbad03ad753e6675f10c7ccd6b1c73e8b`  
		Last Modified: Tue, 10 Jun 2025 23:51:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b25ff85ed811845beb907cc110692448eeb6321798572eca9ab811471a5560ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bae5cc478b21addce1afe15e3ee9b73154bd766dd338d14ba957f037488c48f`

```dockerfile
```

-	Layers:
	-	`sha256:581f061324a158291a461bb0187daaa6832dadf04e7f00cd5f63bf9c29403fda`  
		Last Modified: Wed, 11 Jun 2025 03:35:04 GMT  
		Size: 7.4 MB (7387053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eabf3b159bb1dd4227a3f1984145627e5381c008b8f0cd3547479ce96cc256e6`  
		Last Modified: Wed, 11 Jun 2025 03:35:05 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f595978ee4d8d8f60ad49a5c3ea1d4416223a8869cd7ed4b2f3d8b7d1d4956a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.6 MB (271608279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e49941a33d047daaa6fe0cd22ee4de7661107d81cc8f7183062fcd3ebbf3bbb3`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:8fbf1dd6492cb885c9004e9e7ecb0880a823cd140e63f4b13dfc1bc4d0d3e37b`  
		Last Modified: Tue, 10 Jun 2025 23:26:40 GMT  
		Size: 48.3 MB (48338852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc01628a5303528c749ffb69172a342ad09dcafdc8cafe7b1db49930cb6ed424`  
		Last Modified: Wed, 11 Jun 2025 08:14:11 GMT  
		Size: 142.4 MB (142420681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef396ea42bd9d463025c464db3a3552d2a059f728ab540896d49eb27634f944`  
		Last Modified: Wed, 11 Jun 2025 08:19:57 GMT  
		Size: 80.8 MB (80848102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09e41cae284494455fdfc7d1d1b6bf7420baa37f3bf2cb3f45b55c99b2b2655`  
		Last Modified: Wed, 11 Jun 2025 08:19:38 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:07aff0df4d5530d76ae57905ea9dd59685cde40e694161a028eec534b6395a2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7407803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:200398629d11f0da365f34dad0d0d9cdff001b312a3f02eae7ae4985e0d9b1fd`

```dockerfile
```

-	Layers:
	-	`sha256:a2df77a1d498eb55c67b17713e8d30443bde119e6b586939eb8a25bb415b528e`  
		Last Modified: Wed, 11 Jun 2025 09:35:27 GMT  
		Size: 7.4 MB (7393434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d18123cb45c77cc4bb441c171c8732fd975750984e12ef28141293380350d4b2`  
		Last Modified: Wed, 11 Jun 2025 09:35:28 GMT  
		Size: 14.4 KB (14369 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:5b9c67044d625f680af4fc57e671bf90f2a39a904e2ea04de2af9acda5f2474c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (271961705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baac135ed15a97d043b865f0571f461381f539902dc889dd4ff57f68a0b4c8a0`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
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
	-	`sha256:65d348c3abfb8493d4b77022d58f0afc8e2daa19b2af853f803aef5c836212f9`  
		Last Modified: Tue, 10 Jun 2025 23:28:11 GMT  
		Size: 52.3 MB (52337357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a5bdf4873720215a2424a2b118990a4affb6b25d23f66b192c5876971432ed`  
		Last Modified: Wed, 11 Jun 2025 08:13:18 GMT  
		Size: 132.8 MB (132810531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795c6243ca8d83afe25bec02459f9942d66952749334b1e1c5be31c65110344c`  
		Last Modified: Wed, 11 Jun 2025 08:19:43 GMT  
		Size: 86.8 MB (86813172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e500522b9a96311937ac88b04804e538b92ca66d5ceace6405ad5fe54ff0169`  
		Last Modified: Wed, 11 Jun 2025 08:19:40 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e123adf9a6100aa652daa9ba716ea6e41c72635584d621d612dc4d8ce2c01a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7405942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ff59ce62be6d533178612fcf0720c456940be8416285b4d3ad4cdffa596c8e`

```dockerfile
```

-	Layers:
	-	`sha256:3eb01819e93e1ca450f3772abc0a014d42adaab5a58f58a7eba03b04d990dd25`  
		Last Modified: Wed, 11 Jun 2025 09:35:34 GMT  
		Size: 7.4 MB (7391642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1061f8b37a5ddebdaf544186a5a9672180429a3e89c2f17efa7aee45f69e4e5d`  
		Last Modified: Wed, 11 Jun 2025 09:35:34 GMT  
		Size: 14.3 KB (14300 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:0983d1f53376f1c8c9beeba4c3f1541fd164231c1660c7e15f45242356001207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252538415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8597ec4723e528f80582b77c7013e83ce055a2affd6626b597b503c7596bb2f2`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
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
	-	`sha256:92d876c60c42d9677caf30587cba2266fe6860ddc50efdd0a6fcec154e589f76`  
		Last Modified: Tue, 10 Jun 2025 22:48:13 GMT  
		Size: 47.1 MB (47149408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e658b1e7519f5ff51b5b25baead85f478d24e4eb4e12256bf182b698757a9ec6`  
		Last Modified: Wed, 11 Jun 2025 05:33:46 GMT  
		Size: 125.6 MB (125585329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d32a2cbe50ff2f3b44e2d12ff7ee1a5c36147624fd42c6335bf887f92a361a25`  
		Last Modified: Wed, 11 Jun 2025 05:37:45 GMT  
		Size: 79.8 MB (79803034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd9132cb07d6b0842cbc045e835b7508a3e4a05eb1d0c87de70f8931f2e8109`  
		Last Modified: Wed, 11 Jun 2025 05:37:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d9056e3a3f88c0bef25cec81a39ae5df29a15922fc5fc2b57fc85add7916ac06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a515de734fd8b06f23da7ca2a49e558c248b11f3de948c8668fc8ee7fc5fc284`

```dockerfile
```

-	Layers:
	-	`sha256:cbe6d52e721a6619e1dd4a4414175266120ee1e3a0c46d0cce582561e30e5f23`  
		Last Modified: Wed, 11 Jun 2025 06:35:10 GMT  
		Size: 7.4 MB (7378376 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c7267ea4f7b88d6648dbe1e24cc5aa94c786358e711ae891d8e54ba3b42d044`  
		Last Modified: Wed, 11 Jun 2025 06:35:10 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json
