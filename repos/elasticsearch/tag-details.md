<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:7.17.8`](#elasticsearch7178)
-	[`elasticsearch:8.5.2`](#elasticsearch852)

## `elasticsearch:7.17.8`

```console
$ docker pull elasticsearch@sha256:fdc73b3249c1936f7a277911d58bd10bdd5cf7aae07c1f4d285cf3b7bd18e503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `elasticsearch:7.17.8` - linux; amd64

```console
$ docker pull elasticsearch@sha256:d1b1c87fcd3e6039695f9e67052865ee85568d1be343e26326a6d3b73076b7c0
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.1 MB (354138324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b4df3b1f757e99cb6cee3818f1b9da9a47855741ef06d8b495283d3ad6d9cf2`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Fri, 02 Dec 2022 17:38:29 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Fri, 02 Dec 2022 17:38:30 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch
# Fri, 02 Dec 2022 17:38:30 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 02 Dec 2022 17:38:30 GMT
WORKDIR /usr/share/elasticsearch
# Fri, 02 Dec 2022 17:38:37 GMT
COPY --chown=0:0dir:15beec23a18e3cab272ee0479a77dc21f31bc10561c3eb72a1b84cf33eb522f6 in /usr/share/elasticsearch 
# Fri, 02 Dec 2022 17:38:39 GMT
COPY --chown=0:0file:fcc427e6b1b34164533c7d80cf8bba68e6f09d5c7d442ca055586359d7076e62 in /bin/tini 
# Fri, 02 Dec 2022 17:38:39 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Dec 2022 17:38:39 GMT
COPY file:35bdfc6ad8079cb9cab605169a09ebfe8ce26cd4a9e4120efe12f418073a9bfb in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Dec 2022 17:38:40 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins
# Fri, 02 Dec 2022 17:38:40 GMT
COPY file:12a03e8b4b92c72f58aeb5fcc5d8c6ce94ffb52fa4e13b04e23229fa535fedc0 in /etc/ca-certificates/update.d/docker-openjdk 
# Fri, 02 Dec 2022 17:38:41 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk
# Fri, 02 Dec 2022 17:38:41 GMT
EXPOSE 9200 9300
# Fri, 02 Dec 2022 17:38:41 GMT
LABEL org.label-schema.build-date=2022-12-02T17:33:09.727072865Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=120eabe1c8a0cb2ae87cffc109a5b65d213e9df1 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.8 org.opencontainers.image.created=2022-12-02T17:33:09.727072865Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=120eabe1c8a0cb2ae87cffc109a5b65d213e9df1 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.8
# Fri, 02 Dec 2022 17:38:41 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Fri, 02 Dec 2022 17:38:41 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e247f12a2b5fadf2435dffd0df6cffeee9128409e488ff855ba929842da14620`  
		Last Modified: Thu, 08 Dec 2022 19:22:06 GMT  
		Size: 8.7 MB (8686061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0495283e7099e4d6b1131aff25a580571b82c9d651aa943acb4134202894f67`  
		Last Modified: Thu, 08 Dec 2022 19:22:05 GMT  
		Size: 4.3 KB (4347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7e458ee5994c2382fa67ad3d971d6afd21943861275c2f508639430f61861e`  
		Last Modified: Thu, 08 Dec 2022 19:22:29 GMT  
		Size: 316.6 MB (316563617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00ffe59d0e2690f7196442d2e5098637b854fb5b5908155355d3ed3219ecac53`  
		Last Modified: Thu, 08 Dec 2022 19:22:03 GMT  
		Size: 9.5 KB (9527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab476f874bd0ed85446659b8d33f1e3362c295451579a01d3a9c34caeca103b`  
		Last Modified: Thu, 08 Dec 2022 19:22:03 GMT  
		Size: 2.0 KB (1981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a20df4c47e643927cf82d269360a02b48f1da3c9f690a29973df36207ffa69ee`  
		Last Modified: Thu, 08 Dec 2022 19:22:03 GMT  
		Size: 192.1 KB (192138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef90b430ba5b81dd4918270805f86e347cea0011a15df8349bfd241e3fd8e2cb`  
		Last Modified: Thu, 08 Dec 2022 19:22:03 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79f96f41bfec89084d3adfdf2bcd6f20547fb88df452fac9f241e909800e3d3d`  
		Last Modified: Thu, 08 Dec 2022 19:22:03 GMT  
		Size: 102.4 KB (102413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elasticsearch:7.17.8` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:abb19313e30d1e56f0c2e022cce8ba743215922483c9da5cca04c718e768493e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (351011804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e7a751ed4f0a3ecf2e6f7c0153dc516731336b150e8ed371c8ad6af087d958`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Fri, 02 Dec 2022 17:38:45 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Fri, 02 Dec 2022 17:38:48 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Fri, 02 Dec 2022 17:38:48 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 02 Dec 2022 17:38:48 GMT
WORKDIR /usr/share/elasticsearch
# Fri, 02 Dec 2022 17:38:50 GMT
COPY /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Fri, 02 Dec 2022 17:38:50 GMT
COPY /bin/tini /bin/tini # buildkit
# Fri, 02 Dec 2022 17:38:50 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 02 Dec 2022 17:38:50 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Fri, 02 Dec 2022 17:38:50 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Fri, 02 Dec 2022 17:38:50 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Fri, 02 Dec 2022 17:38:51 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Fri, 02 Dec 2022 17:38:51 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Fri, 02 Dec 2022 17:38:51 GMT
LABEL org.label-schema.build-date=2022-12-02T17:33:09.727072865Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=120eabe1c8a0cb2ae87cffc109a5b65d213e9df1 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=7.17.8 org.opencontainers.image.created=2022-12-02T17:33:09.727072865Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=120eabe1c8a0cb2ae87cffc109a5b65d213e9df1 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=7.17.8
# Fri, 02 Dec 2022 17:38:51 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Fri, 02 Dec 2022 17:38:51 GMT
CMD ["eswrapper"]
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e203ee7abb6500800d9319317105809a398b5be3e3d1130e2178a84b8630daf`  
		Last Modified: Thu, 08 Dec 2022 18:41:16 GMT  
		Size: 8.5 MB (8490726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f33638d7e763d5519b298022ea49693b7d87681bf5f29c4f8ccb03eae2f588fc`  
		Last Modified: Thu, 08 Dec 2022 18:41:15 GMT  
		Size: 4.4 KB (4360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70884ade5b8f9939665241d36329788803d678288f787c0464b856c17190aa3`  
		Last Modified: Thu, 08 Dec 2022 18:41:34 GMT  
		Size: 315.0 MB (315020612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a951d1a6de13fb838fad0ad3a08d924e12b4e930ec79196ac19929d58284259c`  
		Last Modified: Thu, 08 Dec 2022 18:41:12 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9133d822c8166cee37e725eb6556f1cc7f004a7462e03d021a3eade1e14d2b25`  
		Last Modified: Thu, 08 Dec 2022 18:41:12 GMT  
		Size: 2.0 KB (1985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7974d905102e90a77a5ed48be1c49b874b8da5ede1b49e6f194e4e698aeb7f6e`  
		Last Modified: Thu, 08 Dec 2022 18:41:12 GMT  
		Size: 186.2 KB (186165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1befb3933d86201a2a9b3228b65641fec16107722b97d2640fda01f606dd030`  
		Last Modified: Thu, 08 Dec 2022 18:41:12 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf543a5a7fee5a0fb6927ef68b3cfc8d8b79d54898e7dd332d1e20b70ab73624`  
		Last Modified: Thu, 08 Dec 2022 18:41:15 GMT  
		Size: 102.4 KB (102417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `elasticsearch:8.5.2`

```console
$ docker pull elasticsearch@sha256:9ee7fa5787c7372a91d1666c066d57096f293d08eeb029274a294e1dd4f860fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `elasticsearch:8.5.2` - linux; amd64

```console
$ docker pull elasticsearch@sha256:6eb35fbe63877945c363e4bf19b262e0e568987097c0bee7f3229c69fc6bba07
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **623.7 MB (623729394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b19437f14a3b1f662d3e8db30c7eeed88f777314e9dc64be7767f146b2637a67`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Thu, 17 Nov 2022 21:20:35 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Thu, 17 Nov 2022 21:20:36 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch
# Thu, 17 Nov 2022 21:20:36 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 17 Nov 2022 21:20:36 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 17 Nov 2022 21:20:51 GMT
COPY --chown=0:0dir:f108133d18e0681cd7e3b65a58bb4d437bb7acfa107e5504522dbe7ec4928327 in /usr/share/elasticsearch 
# Thu, 17 Nov 2022 21:20:55 GMT
COPY --chown=0:0file:fcc427e6b1b34164533c7d80cf8bba68e6f09d5c7d442ca055586359d7076e62 in /bin/tini 
# Thu, 17 Nov 2022 21:20:55 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Nov 2022 21:20:55 GMT
COPY file:480ac78aea3a6b2b78f3489c03400c7b30d7129a2955fcf04b47c6666f033929 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 17 Nov 2022 21:20:56 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins
# Thu, 17 Nov 2022 21:20:56 GMT
COPY file:12a03e8b4b92c72f58aeb5fcc5d8c6ce94ffb52fa4e13b04e23229fa535fedc0 in /etc/ca-certificates/update.d/docker-openjdk 
# Thu, 17 Nov 2022 21:20:56 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk
# Thu, 17 Nov 2022 21:20:57 GMT
EXPOSE 9200 9300
# Thu, 17 Nov 2022 21:20:57 GMT
LABEL org.label-schema.build-date=2022-11-17T21:17:54.410437150Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=a846182fa16b4ebfcc89aa3c11a11fd5adf3de04 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.5.2 org.opencontainers.image.created=2022-11-17T21:17:54.410437150Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=a846182fa16b4ebfcc89aa3c11a11fd5adf3de04 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.5.2
# Thu, 17 Nov 2022 21:20:57 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 17 Nov 2022 21:20:57 GMT
CMD ["eswrapper"]
# Thu, 17 Nov 2022 21:20:57 GMT
USER elasticsearch:root
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9233316d9dbf357944daebd5aae308fa78615d44b32d3aedf46ec8e762277d5f`  
		Last Modified: Wed, 23 Nov 2022 04:47:01 GMT  
		Size: 7.5 MB (7487571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc27906be4d3a5e49fe2978a29c0f76395265450e59c77c1f1bef36cbcb4602`  
		Last Modified: Wed, 23 Nov 2022 04:47:00 GMT  
		Size: 4.3 KB (4331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f0f50e5d47b1e5729b07f79991d71f0a4b37aa38a255a504838917b074b9cf`  
		Last Modified: Wed, 23 Nov 2022 04:47:49 GMT  
		Size: 587.4 MB (587353718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d069760f90418d3e61dac0a61737d162bbfbf109ab539a4089d26eda139773c8`  
		Last Modified: Wed, 23 Nov 2022 04:46:59 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8e11fd7a9a7e9dad0ee7016e05b2be22c6695b4827237a04bb22c1d52babef`  
		Last Modified: Wed, 23 Nov 2022 04:46:58 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e687db3011a12e1b95f548114be3a6904c17ec34a3002fc1eea612eae0fdbf`  
		Last Modified: Wed, 23 Nov 2022 04:46:58 GMT  
		Size: 191.9 KB (191867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bd12c6dc1ea72e424e3d9a29c2b351139dd35b9a8b679cac3ffa0576890c20`  
		Last Modified: Wed, 23 Nov 2022 04:46:58 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b79bd3f53d9b4fa60e1f3faf83d90f2503587afc272cca137b5f57b309f5f3`  
		Last Modified: Wed, 23 Nov 2022 04:46:58 GMT  
		Size: 102.4 KB (102417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `elasticsearch:8.5.2` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:8537e5cf133402803daf602197d1ca77a1af3e2580eca6ce4b5a35c612f682a2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.1 MB (419115283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3269deb053a47778f53aa0266b8b860ac2aa1a4aadf5584aff82718b1e27806`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 25 Oct 2022 05:54:59 GMT
ADD file:6784d0c4432f4f32d6ee4d96eedf33ea82d88ef6901c763665fa77c842621999 in / 
# Tue, 25 Oct 2022 05:54:59 GMT
CMD ["bash"]
# Thu, 17 Nov 2022 21:22:22 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code
# Thu, 17 Nov 2022 21:22:23 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser --uid 1000 --gid 1000 --home /usr/share/elasticsearch elasticsearch &&     adduser elasticsearch root &&     chown -R 0:0 /usr/share/elasticsearch
# Thu, 17 Nov 2022 21:22:23 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 17 Nov 2022 21:22:23 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 17 Nov 2022 21:22:29 GMT
COPY --chown=0:0dir:19ddff23ed3c3c2da79ab4025094a4fa79f97b7d9c186c9071d0fe025da395b9 in /usr/share/elasticsearch 
# Thu, 17 Nov 2022 21:22:33 GMT
COPY --chown=0:0file:caaa172ee884dfa2de4269dce2215a63f709c6ea183f02cb82e252b7753b9772 in /bin/tini 
# Thu, 17 Nov 2022 21:22:33 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Nov 2022 21:22:33 GMT
COPY file:480ac78aea3a6b2b78f3489c03400c7b30d7129a2955fcf04b47c6666f033929 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 17 Nov 2022 21:22:34 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins
# Thu, 17 Nov 2022 21:22:34 GMT
COPY file:12a03e8b4b92c72f58aeb5fcc5d8c6ce94ffb52fa4e13b04e23229fa535fedc0 in /etc/ca-certificates/update.d/docker-openjdk 
# Thu, 17 Nov 2022 21:22:35 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk
# Thu, 17 Nov 2022 21:22:35 GMT
EXPOSE 9200 9300
# Thu, 17 Nov 2022 21:22:35 GMT
LABEL org.label-schema.build-date=2022-11-17T21:20:04.988417881Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=a846182fa16b4ebfcc89aa3c11a11fd5adf3de04 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.5.2 org.opencontainers.image.created=2022-11-17T21:20:04.988417881Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=a846182fa16b4ebfcc89aa3c11a11fd5adf3de04 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.5.2
# Thu, 17 Nov 2022 21:22:35 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 17 Nov 2022 21:22:35 GMT
CMD ["eswrapper"]
# Thu, 17 Nov 2022 21:22:35 GMT
USER elasticsearch:root
```

-	Layers:
	-	`sha256:4e7e0215f4adc2c48ad9cb3b3781e21d474b477587f85682c2e2975ae91dce9d`  
		Last Modified: Tue, 25 Oct 2022 05:55:59 GMT  
		Size: 27.2 MB (27195998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401c913bec1701f135a611dfc9ce27979d8d8a849a70f3872920cc4ffc14b5af`  
		Last Modified: Tue, 29 Nov 2022 01:47:08 GMT  
		Size: 7.3 MB (7312881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd29d12a258c235540b4ae20e2ea7d4f2a293d7620971ab18b8cb56f96a5bf7`  
		Last Modified: Tue, 29 Nov 2022 01:47:07 GMT  
		Size: 4.4 KB (4370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d714c768053971c5dcd76519b5e33714d13dd1ee4d00b80b9354b1e0f44d6a3e`  
		Last Modified: Tue, 29 Nov 2022 01:47:28 GMT  
		Size: 384.3 MB (384302496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b8ff0d5954a901daeb5ff4be8c1fbef05eecff22bad0ae4f4232b50aa812bc`  
		Last Modified: Tue, 29 Nov 2022 01:47:05 GMT  
		Size: 9.1 KB (9095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1552bec12dc190ea649cdf9e7bac23ba3def87ada2c2c56c37def1d566e0237`  
		Last Modified: Tue, 29 Nov 2022 01:47:05 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466c9ec2d3a13d99fe2ccbbf61b37aa1498e8989529e50790bad6da73e51c77c`  
		Last Modified: Tue, 29 Nov 2022 01:47:05 GMT  
		Size: 185.9 KB (185893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11b03f5b382fea7a12f53a8d670f4350614f20371318f494be8e2582c6487eec`  
		Last Modified: Tue, 29 Nov 2022 01:47:05 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edcc9e88702f44544603c6da98077e7d92d840f83929b81d0d9d7a7eabed3e24`  
		Last Modified: Tue, 29 Nov 2022 01:47:06 GMT  
		Size: 102.4 KB (102417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
