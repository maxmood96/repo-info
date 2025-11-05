## `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim`

```console
$ docker pull clojure@sha256:5680ebee3f6019f22969a738cec64a95846e922e9cc42d98e8550b4231136e46
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

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:6e413a4b426048d4eabcb22424dc23dfc72354c8102a76fd0590326ecd260ee0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243566822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e25fcb4289891e2da6c21a25608a0d09499c99ff1d18f8ed5c364c317679c1dd`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:54:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:54:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:54:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:54:34 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:54:34 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:54:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:54:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:54:49 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866a01a4482d16ef8ed2e1a4a32c1cbf6a9509f493939112011c25bc785bd38d`  
		Last Modified: Wed, 05 Nov 2025 13:39:13 GMT  
		Size: 145.7 MB (145658331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c873e37f0595e3a4121fd2fbe410643d99f6d5066a6258b777bcb3530e49f2b4`  
		Last Modified: Tue, 04 Nov 2025 00:55:35 GMT  
		Size: 69.7 MB (69679279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3c08c276c121e8d5fb8bd4abbe6b2e856ef43cf18ebc818a13bab01303e182`  
		Last Modified: Tue, 04 Nov 2025 00:55:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7b595f018cdb3c388e9af85dd89881036469484846a1af5fa40dbe9eb1ad0312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5147796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39ff1680146c15146b9ca3328bb8c2d2ef06c26a6fb89cfca4d9c8c7f07fe24`

```dockerfile
```

-	Layers:
	-	`sha256:1afbd7b3a9be8b29cb4ee6fe7d351090b347be3cb7dcfa7f019451fb10737b4d`  
		Last Modified: Tue, 04 Nov 2025 10:36:16 GMT  
		Size: 5.1 MB (5133529 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:973b51882041bcfb35f3b0897cdf07d52d01b02365285fc66d618e9849b57d10`  
		Last Modified: Tue, 04 Nov 2025 10:36:17 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:85e117347946c82cfb67721ec24a3003b9e2d5d137ae2c008fbf9ccd6b1e2b90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.1 MB (240123977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e332b6da8c8c8034e01126a8aa31545d007cc20d323298b77b3e6abc7bcb998f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 00:54:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:54:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:54:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:54:56 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:54:56 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:55:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:55:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:55:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af7827a6a51e2d6f86d4c53c622c4e6a123c1340c4737a2b8196e4a3998c161`  
		Last Modified: Wed, 05 Nov 2025 13:39:57 GMT  
		Size: 142.5 MB (142460569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5012d6bca676044051dca10524757bcece26f964c75fb6f30467fa8970315ee`  
		Last Modified: Tue, 04 Nov 2025 00:55:53 GMT  
		Size: 69.6 MB (69560389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63126f89df9c0e2928ab290b63fcb4d4a134a15dc8cdea38e6128a32a8a1895`  
		Last Modified: Tue, 04 Nov 2025 00:55:38 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:051799fa1f97c60b6e350a055b4090e2a99b7900ef9c53f2e2f551608cf6dcbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5154292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9c466e0756c1db6628284f700bf5a8a7f2d1c4e08437ac50a96fa11b068f91`

```dockerfile
```

-	Layers:
	-	`sha256:07b1b12ac248215468af31e19a7cf39b3b30614050f44ffc946ab2e7e0230eb9`  
		Last Modified: Tue, 04 Nov 2025 10:36:22 GMT  
		Size: 5.1 MB (5139908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87ad3ed39f14583646aa8115cedf16aac50f9b2ae39e5dfabd5c988ced3fea26`  
		Last Modified: Tue, 04 Nov 2025 10:36:23 GMT  
		Size: 14.4 KB (14384 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:51086ace769d50da5eddff8c57455ad745df079447199654b3cb22c04b983c97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.4 MB (240435706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80751383130af39f22b76e4a0bb7c463f84fc324550571fab4b70b9fd6cf70fe`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 13:11:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 13:11:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 13:11:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 13:11:37 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 13:11:37 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 13:17:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 13:17:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 13:17:27 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f3bbbc4f3b40bcbfe5e7fa314df78cec7a1321d40bb955ffc7be4fb56243ff`  
		Last Modified: Tue, 04 Nov 2025 23:01:08 GMT  
		Size: 132.9 MB (132853167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1461dafacb125b0c26211ae5ffb6469ffe52ec9192cf3f6e144b61df754b7be3`  
		Last Modified: Tue, 04 Nov 2025 13:18:25 GMT  
		Size: 75.5 MB (75512989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835691be195abd010b5b37ef2a36e514b3219d277e2a3946686898e8e2202e2d`  
		Last Modified: Tue, 04 Nov 2025 13:18:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5cb9562fa4d0a65954e60ccb37b490257db2d44b1dd6b781408dade5a8a55bc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5151586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547f3d8b75e09781737dcd0dc6e78128cfe7930e15dec175f521f66c1490583a`

```dockerfile
```

-	Layers:
	-	`sha256:78b0df9dc2cb38201460766beb857c84d3488addb5f1132bc8d0913c7994dbbe`  
		Last Modified: Tue, 04 Nov 2025 16:35:11 GMT  
		Size: 5.1 MB (5138072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25619386a92959ce2b6dbe0ba0403f2e1dbb027ffc37383db9f67335529d9aab`  
		Last Modified: Tue, 04 Nov 2025 16:35:12 GMT  
		Size: 13.5 KB (13514 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:45b9b1f76b90229be6e9ced867e8d70fd93806eb9060f1a550fb315c2bfa7a30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (220997899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95d9555f96fcdc7ae4f69851b93884d9ea2e00199445d938a95e35f0545912bc`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Tue, 04 Nov 2025 06:20:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 06:20:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 06:20:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 06:20:11 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 06:20:11 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 06:23:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 06:23:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 06:23:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d623a0585b2d2e3a7eed10e762a8ec65ec19fc3d721313f7a566fcb74c84263c`  
		Last Modified: Tue, 04 Nov 2025 06:21:45 GMT  
		Size: 125.6 MB (125622140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6554edfc815adcfa70ba891ba8fd4e24ba12d812efaa51db055376f726184a`  
		Last Modified: Tue, 04 Nov 2025 06:23:52 GMT  
		Size: 68.5 MB (68490563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd95b6ffb2851c981c1370e2da48d61d436b34e273239e136b19eaf002f3fd8e`  
		Last Modified: Tue, 04 Nov 2025 06:23:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:42e4f9fbe9681eac6c2e9b65532497f9ba3fcdbfe93bc04a80446a1832cefad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5138320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591c16d0380718b790e2d848282e7b2610e8177412ad686024d9bd20ba35c621`

```dockerfile
```

-	Layers:
	-	`sha256:a4cf7d7a6fe4e4197637d87c12a99ba01d21a17ab3d80ac5a4a14eceb047a0a5`  
		Last Modified: Tue, 04 Nov 2025 10:36:32 GMT  
		Size: 5.1 MB (5124854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a899dacecc99b5e12234f9a9dc2e7be58e77cb7cf8a4accd95068da8e6c9dad`  
		Last Modified: Tue, 04 Nov 2025 10:36:33 GMT  
		Size: 13.5 KB (13466 bytes)  
		MIME: application/vnd.in-toto+json
