<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `elasticsearch`

-	[`elasticsearch:8.17.10`](#elasticsearch81710)
-	[`elasticsearch:8.18.6`](#elasticsearch8186)
-	[`elasticsearch:8.19.3`](#elasticsearch8193)
-	[`elasticsearch:9.0.6`](#elasticsearch906)
-	[`elasticsearch:9.1.3`](#elasticsearch913)

## `elasticsearch:8.17.10`

```console
$ docker pull elasticsearch@sha256:155f1fe90eddf40b6baf1c1dec236058bc3576023ed6285ff2225512cfa0e828
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.17.10` - linux; amd64

```console
$ docker pull elasticsearch@sha256:735d39468d561bd5702100cdf9cabbeca7835ba1aa37810d3791283b506c10c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **677.0 MB (676958358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c28f992cfab3539abf4de62ce93f674236ae4f80b26835a6ea937a763b148a1`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Aug 2025 08:18:47 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:18:47 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:18:47 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:18:47 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:18:47 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.label-schema.build-date=2025-08-08T08:36:52.872377389Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.10 org.opencontainers.image.created=2025-08-08T08:36:52.872377389Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.10
# Tue, 12 Aug 2025 08:18:47 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 08:18:47 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c165c7a646160f44b8a072a7eddd03084d6965b14246606044b3d9ac3eed32a`  
		Last Modified: Mon, 01 Sep 2025 23:10:05 GMT  
		Size: 4.5 MB (4493679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:806378ff79a7933a0bfb4dd44aeebb5c906eb7293a0c7050d6a443c56a40a206`  
		Last Modified: Mon, 01 Sep 2025 23:10:04 GMT  
		Size: 3.5 KB (3528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7d1e096398acae99195e6b12e4c227b5fd4171f78bf1777d0ade419fb8d09a`  
		Last Modified: Tue, 02 Sep 2025 00:27:27 GMT  
		Size: 642.4 MB (642446922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87eb3109af95e8b3e351751a2e8adeed242f7d40c60ff64b53d5ad6b00f6e74e`  
		Last Modified: Mon, 01 Sep 2025 23:10:04 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d726b63955ce94d5c1ee1616b05b623225aeb7442505f00c802b6bc673dfc78c`  
		Last Modified: Mon, 01 Sep 2025 23:10:04 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694c7cdf811762cbd2a5a46032890a0f09b15520acb89bec463d3853f649ceab`  
		Last Modified: Mon, 01 Sep 2025 23:10:04 GMT  
		Size: 163.9 KB (163937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547b637c8c7831ba72963b41998f2d2fbdb28a871b96b9a49c0cc200dc490555`  
		Last Modified: Mon, 01 Sep 2025 23:10:05 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d029e21ed768b0a699e644429e313ef5bd6d98ef8ae9028c4eca89ea7a7198`  
		Last Modified: Mon, 01 Sep 2025 23:10:04 GMT  
		Size: 115.5 KB (115542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:f0839b20933ec40f479baeabae360757678c340c4684fab1ab1309f7e3c48b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3203176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4c958b1e94844fe82bd76237e6abf81960bddba1791152bf72bc3439337a6ca`

```dockerfile
```

-	Layers:
	-	`sha256:eaa85d15e0879360a29ce1b20bcb5e8679f99cf4ac2aaa673a9dd463316ddae5`  
		Last Modified: Tue, 02 Sep 2025 03:25:24 GMT  
		Size: 3.2 MB (3164781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a9310a5c301b0f3fed84663782a9ef9fa56bd87cd9df420df5dd04804bdce37`  
		Last Modified: Tue, 02 Sep 2025 03:25:25 GMT  
		Size: 38.4 KB (38395 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.17.10` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:70421d1f2927c33550f8084cf229d2865c4af9c37d21746d5c081575205c8eb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **521.2 MB (521163611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:974a94913da3ca38fed95d51cc5c259993b871a5064698341dfafeb48521b28f`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 12 Aug 2025 08:18:47 GMT
ARG RELEASE
# Tue, 12 Aug 2025 08:18:47 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 12 Aug 2025 08:18:47 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["/bin/bash"]
# Tue, 12 Aug 2025 08:18:47 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 Aug 2025 08:18:47 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Aug 2025 08:18:47 GMT
ENV SHELL=/bin/bash
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Tue, 12 Aug 2025 08:18:47 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 12 Aug 2025 08:18:47 GMT
LABEL org.label-schema.build-date=2025-08-08T08:36:52.872377389Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.17.10 org.opencontainers.image.created=2025-08-08T08:36:52.872377389Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=e5c4b2af120c131ea2885730f6693cb7d40a0a63 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.17.10
# Tue, 12 Aug 2025 08:18:47 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 12 Aug 2025 08:18:47 GMT
CMD ["eswrapper"]
# Tue, 12 Aug 2025 08:18:47 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0455cea492cc536bcbe5f171a4b7bfd5e6e5ea914fcbf6c745b633f850d31e5`  
		Last Modified: Tue, 02 Sep 2025 01:10:41 GMT  
		Size: 4.5 MB (4498593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210f4609a81fb730494c0f54e0ee292e756452bd72736b5a9ca1a40c1d1f6937`  
		Last Modified: Tue, 02 Sep 2025 01:10:41 GMT  
		Size: 3.5 KB (3527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f8984123e1cd60065747b170751561d80e138808b18ec5e371b88c6f70808c`  
		Last Modified: Tue, 02 Sep 2025 02:16:22 GMT  
		Size: 487.5 MB (487514092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc63e79d45924beba020d9a355c9d1587cf695c8f14542cc7a141f2e1027dc4`  
		Last Modified: Tue, 02 Sep 2025 01:10:41 GMT  
		Size: 9.1 KB (9102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293aca7c940831e4255629d203b880bd6a684bc8a8ef8a562ee0cd046a051a20`  
		Last Modified: Tue, 02 Sep 2025 01:10:41 GMT  
		Size: 1.7 KB (1716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:718a090f0c5a90eccfcfea8a5fdfda47fe81f82e7f4c7d9388864e83566a0d6d`  
		Last Modified: Tue, 02 Sep 2025 01:10:41 GMT  
		Size: 160.4 KB (160365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5eec739e8c569c15257a1cf88310b8687625d5d0844ecff3aa3ed39e13a617`  
		Last Modified: Tue, 02 Sep 2025 01:10:41 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09b921161b9824c083a45372d4108e9db05de775eb08a76035590d4eb63735a`  
		Last Modified: Tue, 02 Sep 2025 01:10:41 GMT  
		Size: 115.5 KB (115542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.17.10` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:16c5ebe0f3cbb9170cb5463bc0409dc27a6a381b602847f8120a1a719066ca3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3203164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956050138afc35b10db93f97dd7fac06f529796a4a6b3b7c190a964ef6b93b66`

```dockerfile
```

-	Layers:
	-	`sha256:33dea574cb2cb62888eb7ef77c3947f49dddc003920800e28d440ffaa760e971`  
		Last Modified: Tue, 02 Sep 2025 03:25:31 GMT  
		Size: 3.2 MB (3164565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a854b9a86b5b7f68181341782aaab6ad0e87824838a11fabfe8e368e77f295d`  
		Last Modified: Tue, 02 Sep 2025 03:25:32 GMT  
		Size: 38.6 KB (38599 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.18.6`

```console
$ docker pull elasticsearch@sha256:3219fcb7d0ed18b88bc4087b19d48f06205df643d8cce5bf994981718985ab62
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.18.6` - linux; amd64

```console
$ docker pull elasticsearch@sha256:f2176745ca42106eb5fa3f678c0e5bc2500b59221dc72de6981c18d778b87144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **688.3 MB (688337329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aba6d45f8377ddfd432ae354e404897b40b4d6405fdb4a5eb6bf12978bec69ca`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 19 Aug 2025 14:36:58 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:37:00 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 19 Aug 2025 14:37:01 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 08:37:13 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 Aug 2025 08:37:13 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 28 Aug 2025 08:37:13 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Aug 2025 08:37:13 GMT
ENV SHELL=/bin/bash
# Thu, 28 Aug 2025 08:37:13 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 28 Aug 2025 08:37:13 GMT
LABEL org.label-schema.build-date=2025-08-25T22:05:47.180118464Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=970b6c3ae853753ae66a12c1208c85a3c9728d92 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.6 org.opencontainers.image.created=2025-08-25T22:05:47.180118464Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=970b6c3ae853753ae66a12c1208c85a3c9728d92 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.6
# Thu, 28 Aug 2025 08:37:13 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 28 Aug 2025 08:37:13 GMT
CMD ["eswrapper"]
# Thu, 28 Aug 2025 08:37:13 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef9a0161701e33aef4b6897219a025247a3179b75867b5e55c1c1de397c3b6f`  
		Last Modified: Tue, 02 Sep 2025 17:27:55 GMT  
		Size: 4.5 MB (4493672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f36566400679cbe00b2efa3f76efc240362f7db5e85955a0160f89508f9043`  
		Last Modified: Tue, 02 Sep 2025 17:27:56 GMT  
		Size: 3.5 KB (3532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ade8bc94faace97edd4468dc62aa2b022907d38262d76dd823945bbd59e54a8`  
		Last Modified: Tue, 02 Sep 2025 18:33:04 GMT  
		Size: 653.8 MB (653825912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3f53f1167782bf481770f842d0d19187c64bd9eccd0e40d9e0a313a3e654db`  
		Last Modified: Tue, 02 Sep 2025 17:27:56 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf82fac41bd01ac61a7b1417972ccb0c50a0ea6da5e44f36d9d4bad87834626`  
		Last Modified: Tue, 02 Sep 2025 17:27:56 GMT  
		Size: 1.7 KB (1717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0be12f3b877238a565388f505bbe743a43b13a93a908de486105600c7819190`  
		Last Modified: Tue, 02 Sep 2025 17:27:56 GMT  
		Size: 163.9 KB (163930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9d94d50d6aebadf41b905dd991c5ea69e27b3019f9c2830aadbbffcf19daac`  
		Last Modified: Tue, 02 Sep 2025 17:27:56 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3faef9db5178b7bc8e2ba4b0946315f7758fb06973c8997433bd9bbf4a43c7`  
		Last Modified: Tue, 02 Sep 2025 17:27:53 GMT  
		Size: 115.5 KB (115533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:2d58ae5f4d17c0fc9f11597ee2e461778d4a38361fa2196c0d99e7bc95f1ec5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3232775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f778fa80c5245b0def23d494f85d592a20e5a4e9df14b224f55bb6a44b5656c`

```dockerfile
```

-	Layers:
	-	`sha256:0fe57801b237297d2d18e4517fa388675e409bbbfd404b3ddf387b0b30eff2b7`  
		Last Modified: Tue, 02 Sep 2025 18:25:27 GMT  
		Size: 3.2 MB (3194386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:123f1dcd087fc59ff4d7033219102be0fd2839a2fa18c8539d56229e6f28b74c`  
		Last Modified: Tue, 02 Sep 2025 18:25:28 GMT  
		Size: 38.4 KB (38389 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.18.6` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:a3f395cb844909ff7b4f9762eca215be1244397c898f31ab31c0c52dbcf66a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **530.7 MB (530749302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28184871b72f0bb178c368b55d22a8cfbe5764ec6fc970232c910de245a31607`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 19 Aug 2025 14:38:31 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:38:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:38:35 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 19 Aug 2025 14:38:35 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 08:37:13 GMT
RUN yes no | dpkg-reconfigure dash &&     for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 Aug 2025 08:37:13 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 28 Aug 2025 08:37:13 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Aug 2025 08:37:13 GMT
ENV SHELL=/bin/bash
# Thu, 28 Aug 2025 08:37:13 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 28 Aug 2025 08:37:13 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 28 Aug 2025 08:37:13 GMT
LABEL org.label-schema.build-date=2025-08-25T22:05:47.180118464Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=970b6c3ae853753ae66a12c1208c85a3c9728d92 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.18.6 org.opencontainers.image.created=2025-08-25T22:05:47.180118464Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=970b6c3ae853753ae66a12c1208c85a3c9728d92 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.18.6
# Thu, 28 Aug 2025 08:37:13 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 28 Aug 2025 08:37:13 GMT
CMD ["eswrapper"]
# Thu, 28 Aug 2025 08:37:13 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0455cea492cc536bcbe5f171a4b7bfd5e6e5ea914fcbf6c745b633f850d31e5`  
		Last Modified: Tue, 02 Sep 2025 01:10:41 GMT  
		Size: 4.5 MB (4498593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210f4609a81fb730494c0f54e0ee292e756452bd72736b5a9ca1a40c1d1f6937`  
		Last Modified: Tue, 02 Sep 2025 01:10:41 GMT  
		Size: 3.5 KB (3527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0d0bb1ca1dd987d41ed708712bb92cd8904a464fa13c5959bf846fbabd5d2e6`  
		Last Modified: Tue, 02 Sep 2025 17:36:35 GMT  
		Size: 497.1 MB (497099771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d9df2564a8aa7f1d4d24ff85a923baad490c583649403a7857c4fb760ef180`  
		Last Modified: Tue, 02 Sep 2025 17:37:03 GMT  
		Size: 9.1 KB (9105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608f33d32a313df066adb4999ad55f393b55d6b8609dc101ac8be220db10b6cf`  
		Last Modified: Tue, 02 Sep 2025 17:37:02 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fba98b0da85e615b45947bc2d01bf2af8519f28a3d361d1ced85729deb45df0d`  
		Last Modified: Tue, 02 Sep 2025 17:37:02 GMT  
		Size: 160.4 KB (160370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffabb9cfe8d03ad20e7c29934580c0a01a44a68c01803fa4d0cbb0ff3aed221d`  
		Last Modified: Tue, 02 Sep 2025 17:37:03 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f36f0a8ab9df13e21c3c47da991af6d2480d1a49d8aff4281380d50d1f39cd`  
		Last Modified: Tue, 02 Sep 2025 17:37:03 GMT  
		Size: 115.5 KB (115537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.18.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:58b0b666549d41e99a61e5eb1bb704fb8b585d956949c5e7a09d4abd73ffc065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3233391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8013e485f7db72515af9c62daf4c767573d7498b663481e94b7c3fd130f489`

```dockerfile
```

-	Layers:
	-	`sha256:676822423a5738010908588fc474657ea8ddfb6e98b90edd1601276314fd10be`  
		Last Modified: Tue, 02 Sep 2025 18:25:48 GMT  
		Size: 3.2 MB (3194799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6547746e6efb4de62a0972831355be8aa9e3a7625d41ffc7c8084937a5f20446`  
		Last Modified: Tue, 02 Sep 2025 18:25:56 GMT  
		Size: 38.6 KB (38592 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:8.19.3`

```console
$ docker pull elasticsearch@sha256:ed1b91208f1389cbb1dd23f9bdf368667a78a4b34d0edda519debf6d7e05e615
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:8.19.3` - linux; amd64

```console
$ docker pull elasticsearch@sha256:4ca884da59b05d5506e7979c5223aa4d19c761bb580eb8124f02b7cdf25b8d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.1 MB (695060505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:521ef6ebe05f60cb4f5576b06a7ab71805b8e5dd6f2733a2b07420913cd099ed`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 19 Aug 2025 14:36:58 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:36:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:36:58 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:37:00 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 19 Aug 2025 14:37:01 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 08:37:19 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 Aug 2025 08:37:19 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 28 Aug 2025 08:37:19 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Aug 2025 08:37:19 GMT
ENV SHELL=/bin/bash
# Thu, 28 Aug 2025 08:37:19 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 28 Aug 2025 08:37:19 GMT
LABEL org.label-schema.build-date=2025-08-26T02:35:34.366492370Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=1fde05a4d63448377eceb8fd3d51ce16ca3f02a9 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.3 org.opencontainers.image.created=2025-08-26T02:35:34.366492370Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=1fde05a4d63448377eceb8fd3d51ce16ca3f02a9 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.3
# Thu, 28 Aug 2025 08:37:19 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 28 Aug 2025 08:37:19 GMT
CMD ["eswrapper"]
# Thu, 28 Aug 2025 08:37:19 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbdd506418e526fbe57bdd6bb6cd92776cf5665b7ba3559be83369f85165f14d`  
		Last Modified: Tue, 02 Sep 2025 17:27:52 GMT  
		Size: 4.5 MB (4493685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57dd3ba5112a447b84d0229022025c496aa489412bca920146b605921ac469bd`  
		Last Modified: Tue, 02 Sep 2025 17:27:52 GMT  
		Size: 3.5 KB (3528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bdc2c93f2a9b0ed56dfd54f298513ffed7a8ddb61a8e9b8100ccc7172d13e44`  
		Last Modified: Tue, 02 Sep 2025 18:53:44 GMT  
		Size: 660.5 MB (660549077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425287183994787ae79d3cf83f4c632ebb7b9878235e695d01ac49290caf0edf`  
		Last Modified: Tue, 02 Sep 2025 17:27:52 GMT  
		Size: 9.5 KB (9534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5683e0db50c5b9e48c6f909bad6d4dd9383586f531bafbc26f704ce82aca41fc`  
		Last Modified: Tue, 02 Sep 2025 17:27:52 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa20a965f3e6f5717b46f45da622be57ad323017962e6b87e276790f3c0ee193`  
		Last Modified: Tue, 02 Sep 2025 17:27:52 GMT  
		Size: 163.9 KB (163932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce01c726f53b9cfe7d28348cbb02470ab8aedb9f4183fb5fe6f74de0ca91c0ee`  
		Last Modified: Tue, 02 Sep 2025 17:27:52 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7a6aaea321fd277195cfd4acf2190c0873e7655fdc0266d61446f9777a79a6`  
		Last Modified: Tue, 02 Sep 2025 17:27:53 GMT  
		Size: 115.5 KB (115530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:f972baeb9fdf70a7487efb372899ced8eba6e61c4e0e653dd427b631fd534b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3252728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:215947043e1791d451dce41bf6ea569a02db2759c32cb0ee285125d294a1f9ca`

```dockerfile
```

-	Layers:
	-	`sha256:dd6a2123095f65aafdc91e7938535c07decb55c9c7155acb2510fd4d65f72cdf`  
		Last Modified: Tue, 02 Sep 2025 18:25:36 GMT  
		Size: 3.2 MB (3215847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9575a370b5c705d9a8a8fca10f63351b459845936d54261e773eeca3a6e5d13a`  
		Last Modified: Tue, 02 Sep 2025 18:25:37 GMT  
		Size: 36.9 KB (36881 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:8.19.3` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:8f8ac49f3608e2a8294eeaa65650639c83f1a580ce11bd1429bde2913e41b08a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **537.5 MB (537456528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:924d78bae97ef2315b8c79f722283e52818cde6d9342910d29cff76d555fa5b4`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Tue, 19 Aug 2025 14:38:31 GMT
ARG RELEASE
# Tue, 19 Aug 2025 14:38:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 14:38:32 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 19 Aug 2025 14:38:35 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 19 Aug 2025 14:38:35 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 08:37:19 GMT
RUN yes no | dpkg-reconfigure dash && for iter in 1 2 3 4 5 6 7 8 9 10; do       export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get upgrade -y &&       apt-get install -y --no-install-recommends         ca-certificates curl netcat-openbsd p11-kit unzip zip  &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* &&       exit_code=0 && break ||         exit_code=$? && echo "apt-get error: retry $iter in 10s" && sleep 10;     done;     exit $exit_code # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN userdel -r ubuntu &&     groupadd -g 1000 elasticsearch &&     useradd --uid 1000 --gid 1000 --home-dir /usr/share/elasticsearch --create-home elasticsearch &&     usermod -aG root elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
ENV ELASTIC_CONTAINER=true
# Thu, 28 Aug 2025 08:37:19 GMT
WORKDIR /usr/share/elasticsearch
# Thu, 28 Aug 2025 08:37:19 GMT
COPY --chown=0:0 /usr/share/elasticsearch /usr/share/elasticsearch # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Aug 2025 08:37:19 GMT
ENV SHELL=/bin/bash
# Thu, 28 Aug 2025 08:37:19 GMT
COPY bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN chmod g=u /etc/passwd &&     chmod 0555 /usr/local/bin/docker-entrypoint.sh &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
COPY bin/docker-openjdk /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
RUN /etc/ca-certificates/update.d/docker-openjdk # buildkit
# Thu, 28 Aug 2025 08:37:19 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Thu, 28 Aug 2025 08:37:19 GMT
LABEL org.label-schema.build-date=2025-08-26T02:35:34.366492370Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=1fde05a4d63448377eceb8fd3d51ce16ca3f02a9 org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=8.19.3 org.opencontainers.image.created=2025-08-26T02:35:34.366492370Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=1fde05a4d63448377eceb8fd3d51ce16ca3f02a9 org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.3
# Thu, 28 Aug 2025 08:37:19 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Thu, 28 Aug 2025 08:37:19 GMT
CMD ["eswrapper"]
# Thu, 28 Aug 2025 08:37:19 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f16f5301b8771135a56997cb07b9dfd4f910447ab2311e639457a0c697c4cab`  
		Last Modified: Tue, 02 Sep 2025 01:15:00 GMT  
		Size: 4.5 MB (4498579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02d2ccf21c2e0288fcfc3e1a3dc3f0ccf72fceaa0992eff983d88cebfd5e5eff`  
		Last Modified: Tue, 02 Sep 2025 01:14:59 GMT  
		Size: 3.5 KB (3527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463a32f9f5e92227567e33747af63c1847f709a07d80268ec46aa8d6b777b99c`  
		Last Modified: Tue, 02 Sep 2025 18:32:29 GMT  
		Size: 503.8 MB (503807010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad623ea80ba0628dad94167aef7e51cc53ad2209d873c151c17d77bf74ca9ce`  
		Last Modified: Tue, 02 Sep 2025 17:39:16 GMT  
		Size: 9.1 KB (9105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:903f31ddbbe94f4e4db795eed432549a397f19c0e006217843ce707e70858508`  
		Last Modified: Tue, 02 Sep 2025 17:39:15 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c585235191d0d066b865ef330bd78dae9cb2c2b846dc075c688106369123f3`  
		Last Modified: Tue, 02 Sep 2025 17:39:16 GMT  
		Size: 160.4 KB (160373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08148f3a26c213b39ef139dc6dc22d39e6991fe42daecb0aa0fc482bd3af8838`  
		Last Modified: Tue, 02 Sep 2025 17:39:16 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e63dc5242d4c24328ca9423bc086120cf71242d2bd881e9a0e6951325234b42`  
		Last Modified: Tue, 02 Sep 2025 17:39:17 GMT  
		Size: 115.5 KB (115536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:8.19.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:393ed4ab278303767c9e12b1c4a601b62960757fd293754bf2e0d6c158ccc61d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3253345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3585a432aec2b6df86b165dc7f3b359bb649448264dec223c91fc808ed347598`

```dockerfile
```

-	Layers:
	-	`sha256:377b118d7e20484ebd62f4e853032146238e1e193e36d41050392236f2ed54c7`  
		Last Modified: Tue, 02 Sep 2025 18:25:41 GMT  
		Size: 3.2 MB (3216260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c748fdb5f6b2ab67023fbf3c1b4c8c79910de79af575b63b40e4b0f10b48d4e5`  
		Last Modified: Tue, 02 Sep 2025 18:25:42 GMT  
		Size: 37.1 KB (37085 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.0.6`

```console
$ docker pull elasticsearch@sha256:8c966f6b7e8c2b646b2aca339263ea019dd53408fe3dc4371e7550c27336a6e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.0.6` - linux; amd64

```console
$ docker pull elasticsearch@sha256:0e9d62c371d89dc839a3b3c615063544a1b967e89b6dff21d3e05186307986bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **700.4 MB (700375639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f10a565d6b7456a0c01710cdd56555baf82af26a9d01300b4f551a9144c1c7`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 20 Aug 2025 13:14:25 GMT
ENV container oci
# Wed, 20 Aug 2025 13:14:25 GMT
COPY dir:e1f22eafd6489859288910ef7585f9d694693aa84a31ba9d54dea9e7a451abe6 in / 
# Wed, 20 Aug 2025 13:14:26 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 20 Aug 2025 13:14:26 GMT
CMD ["/bin/bash"]
# Wed, 20 Aug 2025 13:14:26 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Wed, 20 Aug 2025 13:14:26 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Wed, 20 Aug 2025 13:14:26 GMT
LABEL "build-date"="2025-08-20T13:12:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 02 Sep 2025 11:31:20 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Sep 2025 11:31:20 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 02 Sep 2025 11:31:20 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 11:31:20 GMT
ENV SHELL=/bin/bash
# Tue, 02 Sep 2025 11:31:20 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 02 Sep 2025 11:31:20 GMT
LABEL org.label-schema.build-date=2025-08-24T22:05:07.219522691Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c519c0e3cfc2464e0eb0c09996b683e40b4235cd org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.0.6 org.opencontainers.image.created=2025-08-24T22:05:07.219522691Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c519c0e3cfc2464e0eb0c09996b683e40b4235cd org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.6
# Tue, 02 Sep 2025 11:31:20 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.0.6 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 02 Sep 2025 11:31:20 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 02 Sep 2025 11:31:20 GMT
CMD ["eswrapper"]
# Tue, 02 Sep 2025 11:31:20 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1e02d32990adc4dad7c8927f91cca33a1baba746105504093311eb3b0b691fa0`  
		Last Modified: Wed, 20 Aug 2025 15:04:59 GMT  
		Size: 39.6 MB (39647287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d46736b3e58617d122395d8f3624f6f60a386aba11eb4a3534c9c5969bfae3`  
		Last Modified: Tue, 02 Sep 2025 17:27:47 GMT  
		Size: 4.3 MB (4284033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ccd3df6c185ae86c9b0fc7e31664f62dd6d34e7e4e3334c2c257105fb3a944`  
		Last Modified: Tue, 02 Sep 2025 17:27:47 GMT  
		Size: 1.5 KB (1533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8301d5428865fe5f4a9e423864cde550f44a31754791e252f1f3ae15cbbc3717`  
		Last Modified: Tue, 02 Sep 2025 17:27:47 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f2b208405214a1b97165d0cd32f811e47477c77f9fcc460a83cdd7bd0601c3`  
		Last Modified: Tue, 02 Sep 2025 18:33:00 GMT  
		Size: 656.4 MB (656353796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f170040cd179e0074d6bf64211dd609ad2479055485fb3148d6fb7e712b9ab8e`  
		Last Modified: Tue, 02 Sep 2025 17:27:47 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7273961c01ba13cdad616af13011a5eb7024e4d44a4e8d68a7a0f2d85c7da8`  
		Last Modified: Tue, 02 Sep 2025 17:27:48 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b73cac8be0e12defb736d722cda585b9cb860df583877a69c0f564f1abafa32c`  
		Last Modified: Tue, 02 Sep 2025 17:27:48 GMT  
		Size: 75.7 KB (75742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0030095da2b3a5a91ea1591ebf756a6c62b86e11631c522e2a78423c09c49295`  
		Last Modified: Tue, 02 Sep 2025 17:27:48 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:a89056473b84c35c7be13003933515fc65a4c9fd55df15fe621afe1df2680508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2064538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d15dc968b1221a71c861fc28a02c2d80dd2eeee2b26ebc671102563e2fd779f`

```dockerfile
```

-	Layers:
	-	`sha256:9eee949ca729638280384e458561f4247c66efed100dee02447b6e19071efb71`  
		Last Modified: Tue, 02 Sep 2025 18:25:39 GMT  
		Size: 2.0 MB (2030699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0125f6ebc36f3d5e5b24cbf9d6a3cc5860d8e20cae597b3d017ee43e0ed661ed`  
		Last Modified: Tue, 02 Sep 2025 18:25:40 GMT  
		Size: 33.8 KB (33839 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.0.6` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:839fcba3e2d5e13eeb3b355003a93823987285b30515b239cb804d8169eb123c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **538.9 MB (538858729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae411ab7b89364f2f95c07829d8301ba907d5807c98f578b901660506b2b8b2c`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.openshift.expose-services=""
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 20 Aug 2025 13:15:03 GMT
ENV container oci
# Wed, 20 Aug 2025 13:15:04 GMT
COPY dir:f91aecd64a5df0b73e2b5740ae90f4bb03c2e87890175a65862ca830f6caced5 in / 
# Wed, 20 Aug 2025 13:15:04 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 20 Aug 2025 13:15:04 GMT
CMD ["/bin/bash"]
# Wed, 20 Aug 2025 13:15:04 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Wed, 20 Aug 2025 13:15:04 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Wed, 20 Aug 2025 13:15:04 GMT
LABEL "build-date"="2025-08-20T13:14:46" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 02 Sep 2025 11:31:20 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Sep 2025 11:31:20 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 02 Sep 2025 11:31:20 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 11:31:20 GMT
ENV SHELL=/bin/bash
# Tue, 02 Sep 2025 11:31:20 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 02 Sep 2025 11:31:20 GMT
LABEL org.label-schema.build-date=2025-08-24T22:05:07.219522691Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=c519c0e3cfc2464e0eb0c09996b683e40b4235cd org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.0.6 org.opencontainers.image.created=2025-08-24T22:05:07.219522691Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=c519c0e3cfc2464e0eb0c09996b683e40b4235cd org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.0.6
# Tue, 02 Sep 2025 11:31:20 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.0.6 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 02 Sep 2025 11:31:20 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Sep 2025 11:31:20 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 02 Sep 2025 11:31:20 GMT
CMD ["eswrapper"]
# Tue, 02 Sep 2025 11:31:20 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:73ac460760dbc07b4e932677ed1d86c86c51259cd8ea7c5f1d5b13c9dd3d9d59`  
		Last Modified: Wed, 20 Aug 2025 18:13:24 GMT  
		Size: 37.9 MB (37859581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6cfb60ffc9315a7fd95e258b3d01246ce21f14bb090c028e75c366fb7b4b2f`  
		Last Modified: Tue, 02 Sep 2025 17:41:47 GMT  
		Size: 4.3 MB (4293014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81385e4903430b053f077f100e40110ff1c9b830f526f5fd39f58841d2dac29`  
		Last Modified: Tue, 02 Sep 2025 17:41:50 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ab5703ca385b2f0da76e0dd71463d310b61d145e5f0bc29c2a8d479a8b16d6`  
		Last Modified: Tue, 02 Sep 2025 17:41:50 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64994d71f229bafc908a81be757f2d3eafb9a7c6139afb8141c6b1171ccc6278`  
		Last Modified: Tue, 02 Sep 2025 18:34:08 GMT  
		Size: 496.6 MB (496617157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8864b7a6faec871870be8af4a76df45e1d23fdeb1acd60ef8554e629be15ae8`  
		Last Modified: Tue, 02 Sep 2025 17:41:51 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76ae2e2dcb02eedf494e14188dddf7e5605079555734571e9eafec448ee1578`  
		Last Modified: Tue, 02 Sep 2025 17:41:51 GMT  
		Size: 1.7 KB (1721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f4d3d95b187bd488511682f1bf72104a8e339197741ad3831b4acc6447cae6`  
		Last Modified: Tue, 02 Sep 2025 17:41:52 GMT  
		Size: 74.6 KB (74634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b3ad77e79de4aa3de442ca63ad5cf8bb82673770edb9d7b5d546afc009c59b`  
		Last Modified: Tue, 02 Sep 2025 17:41:52 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.0.6` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:20164798083e83ab2c37e9c06cecd2e6bec042f4be74bb94ef68756ed1094c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2065284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec5b1918884bbe94694d135aff62033646c59ea3c37e1db519f5fd0df7b6170d`

```dockerfile
```

-	Layers:
	-	`sha256:642499e6dedc2ecc643d49b192c1ec0e4053944a45fafc68c2df62db78398560`  
		Last Modified: Tue, 02 Sep 2025 18:25:45 GMT  
		Size: 2.0 MB (2031263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f7cf3c58c94ec9e600000aee5b120f31326fa196c4f6255e05b52fe4f708dd1`  
		Last Modified: Tue, 02 Sep 2025 18:25:46 GMT  
		Size: 34.0 KB (34021 bytes)  
		MIME: application/vnd.in-toto+json

## `elasticsearch:9.1.3`

```console
$ docker pull elasticsearch@sha256:05069ffdf546dbb8d1e3f1b9fcf0d8d7e9aa9164d4b85153936e356a4173aba9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `elasticsearch:9.1.3` - linux; amd64

```console
$ docker pull elasticsearch@sha256:6177bc87b6ea5e0d63c872707080699feaf6edac41c7f4cca04c7677bce36f1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **715.2 MB (715231610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6895cd1669fe448ee82e6ed45791ce2c24ab0f2088f3b34040edc0ec90d3c216`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 20 Aug 2025 13:14:24 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.openshift.expose-services=""
# Wed, 20 Aug 2025 13:14:25 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 20 Aug 2025 13:14:25 GMT
ENV container oci
# Wed, 20 Aug 2025 13:14:25 GMT
COPY dir:e1f22eafd6489859288910ef7585f9d694693aa84a31ba9d54dea9e7a451abe6 in / 
# Wed, 20 Aug 2025 13:14:26 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 20 Aug 2025 13:14:26 GMT
CMD ["/bin/bash"]
# Wed, 20 Aug 2025 13:14:26 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /usr/share/buildinfo/content-sets.json 
# Wed, 20 Aug 2025 13:14:26 GMT
COPY file:58cc94f5b3b2d60de2c77a6ed4b1797dcede502ccdb429a72e7a72d994235b3c in /root/buildinfo/content_manifests/content-sets.json 
# Wed, 20 Aug 2025 13:14:26 GMT
LABEL "build-date"="2025-08-20T13:12:41" "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 02 Sep 2025 11:31:33 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Sep 2025 11:31:33 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 02 Sep 2025 11:31:33 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 11:31:33 GMT
ENV SHELL=/bin/bash
# Tue, 02 Sep 2025 11:31:33 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 02 Sep 2025 11:31:33 GMT
LABEL org.label-schema.build-date=2025-08-24T22:05:04.526302670Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=0c781091a2f57de895a73a1391ff8426c0153c8d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.3 org.opencontainers.image.created=2025-08-24T22:05:04.526302670Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=0c781091a2f57de895a73a1391ff8426c0153c8d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.3
# Tue, 02 Sep 2025 11:31:33 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.3 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 02 Sep 2025 11:31:33 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 02 Sep 2025 11:31:33 GMT
CMD ["eswrapper"]
# Tue, 02 Sep 2025 11:31:33 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:1e02d32990adc4dad7c8927f91cca33a1baba746105504093311eb3b0b691fa0`  
		Last Modified: Wed, 20 Aug 2025 15:04:59 GMT  
		Size: 39.6 MB (39647287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:934d714799cb80a828c44d158d5f12e8d6f94b696fa1cdce3a1d36d389bb2f74`  
		Last Modified: Tue, 02 Sep 2025 17:27:59 GMT  
		Size: 4.3 MB (4283952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8444b85a0601e8d51456a957e6adbedc16081a7b215083c8909bdbe38e172a`  
		Last Modified: Tue, 02 Sep 2025 17:27:58 GMT  
		Size: 1.5 KB (1532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9bcecba2266577b8bcc570b90a72f17d78bc155909d1ae7dae5104b380e45f`  
		Last Modified: Tue, 02 Sep 2025 17:27:58 GMT  
		Size: 9.5 KB (9533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32c6c73a671c7e6c01cac0be9471cb573724e615467d9648ac66039748958b6`  
		Last Modified: Tue, 02 Sep 2025 18:29:17 GMT  
		Size: 671.2 MB (671209844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a10648d3eed4cece6e8ec49b3e1b56ab9c289588a73a6b5dcaf0f8b930d12b`  
		Last Modified: Tue, 02 Sep 2025 17:27:58 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb93096ef8e76ce06f4511374a4d27e1e57d0cde23b29e6c841f002a07a31d8`  
		Last Modified: Tue, 02 Sep 2025 17:27:59 GMT  
		Size: 1.7 KB (1719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b4ee2f76d34b136891bde98bb80fb34bd95860928d33be648bf8e9fccb5037`  
		Last Modified: Tue, 02 Sep 2025 17:27:59 GMT  
		Size: 75.7 KB (75745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d5cd140d2a30379e02f13190b772e9e6756da848708d3720c07f537736ea20`  
		Last Modified: Tue, 02 Sep 2025 17:27:58 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:ee599de1b09bd7cf00f883e883f1972e9594cf4bc03119740df1b6d4993f5f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2118897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a918d3edb0822af3b32034752d4f7672da9b763f4dd2933bb7f7c11fea8969c3`

```dockerfile
```

-	Layers:
	-	`sha256:d5aacb34a19c936aeaac5d23d8e6c9470302842c09c51642e51f51ee702da1ab`  
		Last Modified: Tue, 02 Sep 2025 18:25:50 GMT  
		Size: 2.1 MB (2085058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5debb9c28c2675693b2fa55886c9920c5b089fcaa79dfa94b769d4559f7b0183`  
		Last Modified: Tue, 02 Sep 2025 18:25:52 GMT  
		Size: 33.8 KB (33839 bytes)  
		MIME: application/vnd.in-toto+json

### `elasticsearch:9.1.3` - linux; arm64 variant v8

```console
$ docker pull elasticsearch@sha256:9a497f5637477f0f3d34419e602023a3aed1d8be9db8638092963b1b919b302d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **553.7 MB (553705656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f02e88a1e9a725987a8aa7d62108f39867d28cc411147936fd8ca5eab5275107`
-	Entrypoint: `["\/bin\/tini","--","\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["eswrapper"]`

```dockerfile
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL maintainer="Red Hat, Inc."
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL vendor="Red Hat, Inc."
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9-minimal"       version="9.6"       distribution-scope="public"
# Wed, 20 Aug 2025 13:15:02 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.openshift.expose-services=""
# Wed, 20 Aug 2025 13:15:03 GMT
LABEL io.openshift.tags="minimal rhel9"
# Wed, 20 Aug 2025 13:15:03 GMT
ENV container oci
# Wed, 20 Aug 2025 13:15:04 GMT
COPY dir:f91aecd64a5df0b73e2b5740ae90f4bb03c2e87890175a65862ca830f6caced5 in / 
# Wed, 20 Aug 2025 13:15:04 GMT
COPY file:b37d593713ee21ad52a4cd1424dc019a24f7966f85df0ac4b86d234302695328 in /etc/yum.repos.d/. 
# Wed, 20 Aug 2025 13:15:04 GMT
CMD ["/bin/bash"]
# Wed, 20 Aug 2025 13:15:04 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /usr/share/buildinfo/content-sets.json 
# Wed, 20 Aug 2025 13:15:04 GMT
COPY file:0667e9d31385a24c3aef13f2dd9ab6a7b71b3dfcfef5127d3c1e2ea2c838e5cb in /root/buildinfo/content_manifests/content-sets.json 
# Wed, 20 Aug 2025 13:15:04 GMT
LABEL "build-date"="2025-08-20T13:14:46" "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="f4b088292653bbf5ca8188a5e59ffd06a8671d4b" "release"="1755695350"
# Tue, 02 Sep 2025 11:31:33 GMT
RUN microdnf install --setopt=tsflags=nodocs -y     nc shadow-utils zip unzip findutils procps-ng &&     microdnf clean all # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
RUN groupadd -g 1000 elasticsearch &&     adduser -u 1000 -g 1000 -G 0 -d /usr/share/elasticsearch elasticsearch &&     chown -R 0:0 /usr/share/elasticsearch # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 02 Sep 2025 11:31:33 GMT
COPY /bin/tini /bin/tini # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
WORKDIR /usr/share/elasticsearch
# Tue, 02 Sep 2025 11:31:33 GMT
COPY --chown=0:0 /usr/share/elasticsearch . # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
RUN ln -sf /etc/pki/ca-trust/extracted/java/cacerts jdk/lib/security/cacerts # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
ENV PATH=/usr/share/elasticsearch/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Sep 2025 11:31:33 GMT
ENV SHELL=/bin/bash
# Tue, 02 Sep 2025 11:31:33 GMT
COPY --chmod=0555 bin/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
RUN chmod g=u /etc/passwd &&     find / -xdev -perm -4000 -exec chmod ug-s {} + &&     chmod 0775 /usr/share/elasticsearch &&     chown elasticsearch bin config config/jvm.options.d data logs plugins # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
EXPOSE map[9200/tcp:{} 9300/tcp:{}]
# Tue, 02 Sep 2025 11:31:33 GMT
LABEL org.label-schema.build-date=2025-08-24T22:05:04.526302670Z org.label-schema.license=Elastic-License-2.0 org.label-schema.name=Elasticsearch org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/elasticsearch org.label-schema.usage=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.label-schema.vcs-ref=0c781091a2f57de895a73a1391ff8426c0153c8d org.label-schema.vcs-url=https://github.com/elastic/elasticsearch org.label-schema.vendor=Elastic org.label-schema.version=9.1.3 org.opencontainers.image.created=2025-08-24T22:05:04.526302670Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/elasticsearch/reference/index.html org.opencontainers.image.licenses=Elastic-License-2.0 org.opencontainers.image.revision=0c781091a2f57de895a73a1391ff8426c0153c8d org.opencontainers.image.source=https://github.com/elastic/elasticsearch org.opencontainers.image.title=Elasticsearch org.opencontainers.image.url=https://www.elastic.co/products/elasticsearch org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.1.3
# Tue, 02 Sep 2025 11:31:33 GMT
LABEL name=Elasticsearch maintainer=infra@elastic.co vendor=Elastic version=9.1.3 release=1 summary=Elasticsearch description=You know, for search.
# Tue, 02 Sep 2025 11:31:33 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Tue, 02 Sep 2025 11:31:33 GMT
ENTRYPOINT ["/bin/tini" "--" "/usr/local/bin/docker-entrypoint.sh"]
# Tue, 02 Sep 2025 11:31:33 GMT
CMD ["eswrapper"]
# Tue, 02 Sep 2025 11:31:33 GMT
USER 1000:0
```

-	Layers:
	-	`sha256:73ac460760dbc07b4e932677ed1d86c86c51259cd8ea7c5f1d5b13c9dd3d9d59`  
		Last Modified: Wed, 20 Aug 2025 18:13:24 GMT  
		Size: 37.9 MB (37859581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6cfb60ffc9315a7fd95e258b3d01246ce21f14bb090c028e75c366fb7b4b2f`  
		Last Modified: Tue, 02 Sep 2025 17:41:47 GMT  
		Size: 4.3 MB (4293014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81385e4903430b053f077f100e40110ff1c9b830f526f5fd39f58841d2dac29`  
		Last Modified: Tue, 02 Sep 2025 17:41:50 GMT  
		Size: 1.5 KB (1527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ab5703ca385b2f0da76e0dd71463d310b61d145e5f0bc29c2a8d479a8b16d6`  
		Last Modified: Tue, 02 Sep 2025 17:41:50 GMT  
		Size: 9.1 KB (9101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62999c8aeab0e608f469daffec1b6b3094a94b1699e32f8c32c647276310b9c`  
		Last Modified: Tue, 02 Sep 2025 18:33:33 GMT  
		Size: 511.5 MB (511464078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d208372b1b8ebfd845e5797227be62b51e760933411409562fbd42404b1a9675`  
		Last Modified: Tue, 02 Sep 2025 17:43:51 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8235ff51b49b0b3abdcff1eb3db303ba2461385342ec449f162d51657dc9f8c4`  
		Last Modified: Tue, 02 Sep 2025 17:43:51 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e058de940a26a581fb5953162ca5b3a724f7d143facd7ec125af8cf1a965674`  
		Last Modified: Tue, 02 Sep 2025 17:43:51 GMT  
		Size: 74.6 KB (74639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84979c2afd670a0b04441a98402f4ccd1292e567a526e9ebbdc457acc999f38`  
		Last Modified: Tue, 02 Sep 2025 17:43:52 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `elasticsearch:9.1.3` - unknown; unknown

```console
$ docker pull elasticsearch@sha256:917f03333a8b3e0eac59737dad483fe3bc94996d3e6605553801f09646688668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2119643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf30c206aa8531aac99452724008a689eae75f51a1a171e2324c2e8e91bb58e`

```dockerfile
```

-	Layers:
	-	`sha256:739ed8b2789cc736592f591447fcb2607821bbfa5726173291adfc4f4a3ffdd3`  
		Last Modified: Tue, 02 Sep 2025 18:25:56 GMT  
		Size: 2.1 MB (2085622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40682fb5517826b7eb3f3182e71a8a397fd49b5f1cbcd768cf1775955ef53c39`  
		Last Modified: Tue, 02 Sep 2025 18:25:57 GMT  
		Size: 34.0 KB (34021 bytes)  
		MIME: application/vnd.in-toto+json
