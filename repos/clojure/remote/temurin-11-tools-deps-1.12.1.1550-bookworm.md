## `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm`

```console
$ docker pull clojure@sha256:98cb639fee462e28c99b97e77404c8aaa4268a176ccdad5b4bd6eda8ecc7be0b
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

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm` - linux; amd64

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

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:acba0cddbad11d722a6493afa6cbe45c30e3d834d424e7d6076e73c04e852764
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.6 MB (271596763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d6d13c74377d8f4672d4ad5d4cf9fa792e5bb8603f19d24f3175312d0c96a8d`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:1a12b4ea7c0ce04aa0e98be0a8c9942162bac71426f734fe6d3bf988bc9e2627`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 48.3 MB (48327181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07fd337589b0c96f06ac5d8a22e233b7ae5c98928b27c342b7ea0174f5098e96`  
		Last Modified: Fri, 06 Jun 2025 13:20:07 GMT  
		Size: 142.4 MB (142420644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81efd9728c9f144550bb2175a9b45c2759984d22fea4e6b4cef900bd490dd762`  
		Last Modified: Mon, 09 Jun 2025 17:39:20 GMT  
		Size: 80.8 MB (80848293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc555beaa2ac46150a7f4b506cccc39c88aadaf2c31198fa7f9a850a4f5375d`  
		Last Modified: Mon, 09 Jun 2025 17:39:09 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b2a1f2e92277cd6283f46f890aa9f0b955046a84ce7fa221a6f100ba9db2ed6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7407803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae18d357b95c7eda0ba7f0d3197cd10e3c9fad885a238a204fc1cb385dfd6eed`

```dockerfile
```

-	Layers:
	-	`sha256:ed9f831f2d04ed9b10baa849f1109cd78b230aec15ed0b9a218a71c46193d9fe`  
		Last Modified: Mon, 09 Jun 2025 18:34:58 GMT  
		Size: 7.4 MB (7393434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee037db6f82cb95263f87911f2f339c74272b5ac540726ccc3078b63981c66a0`  
		Last Modified: Mon, 09 Jun 2025 18:34:59 GMT  
		Size: 14.4 KB (14369 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:7b858401dfae496e1286ff1fe8f9fb75b2ac7ee83b735f208d637c36eb5686e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (271956207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3fc1343a16b6a2b61ba7de5aba0d761c831c7b9ed37be844ed6933d530d9dc`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
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
	-	`sha256:996840ee350796081b3c80118ca1a58ce8212c6fdf88c454706a16457903a0c9`  
		Last Modified: Tue, 03 Jun 2025 13:33:40 GMT  
		Size: 52.3 MB (52331619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc84d937b9f9c6a8fdf10268fbf36f3f3530d2d16cd85cb8e98d71c60b41b51`  
		Last Modified: Mon, 09 Jun 2025 19:58:38 GMT  
		Size: 132.8 MB (132810522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d57bfb8583c54fbe202b8e8bcc6d0883ed7347ee0174001d0f9a49a6cfd0332`  
		Last Modified: Mon, 09 Jun 2025 17:50:50 GMT  
		Size: 86.8 MB (86813421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04478a98487575969670fd77f5dc87072e2be9049d6aaeebaef0ea6c329596f2`  
		Last Modified: Mon, 09 Jun 2025 17:50:40 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bd28909e6f8cde1f1c62229a2fa019380448ce7c110e02059be9098bfb39775a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7405942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0007fd90ed581709933bf068b8527c26df5cfe29be1ab470eddc82bfb8ce679a`

```dockerfile
```

-	Layers:
	-	`sha256:5563475d5ba9f434e3c3d653461ec3d4f42efd77bdb5d0c3722484737ce336a6`  
		Last Modified: Mon, 09 Jun 2025 18:35:06 GMT  
		Size: 7.4 MB (7391642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc3b5b1c2873053f8693210a9af87331ddde0cdf7a0179087db4be39714a6c6`  
		Last Modified: Mon, 09 Jun 2025 18:35:07 GMT  
		Size: 14.3 KB (14300 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm` - linux; s390x

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

### `clojure:temurin-11-tools-deps-1.12.1.1550-bookworm` - unknown; unknown

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
