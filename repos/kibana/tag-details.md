<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:8.19.13`](#kibana81913)
-	[`kibana:9.2.7`](#kibana927)
-	[`kibana:9.3.2`](#kibana932)

## `kibana:8.19.13`

```console
$ docker pull kibana@sha256:7e55cb0bf473fdbe1d26448f1773de0d9b0eb6aeea35298b6c6291bc781fc1c6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:8.19.13` - linux; amd64

```console
$ docker pull kibana@sha256:24ecdb31410e2cd3e1c203f4bc564ec93069511da0d6ffa5d88c43ca6859cdb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.2 MB (463227978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:915463491b7ac94f8c04e8df216cf46573d5291502a1433d717fb6d89d1b3ffb`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 03 Apr 2026 15:16:40 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:16:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:16:40 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:16:42 GMT
ADD file:0f6466425c4f1800aae9224ddc3437b90c829cea58fb8edd5dde2f1eb0ee28da in / 
# Fri, 03 Apr 2026 15:16:43 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 01:58:40 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 07 Apr 2026 01:58:40 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:08:10 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 07 Apr 2026 02:08:11 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 07 Apr 2026 02:08:11 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 07 Apr 2026 02:08:11 GMT
RUN fc-cache -v # buildkit
# Tue, 07 Apr 2026 02:08:11 GMT
WORKDIR /usr/share/kibana
# Tue, 07 Apr 2026 02:08:11 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 07 Apr 2026 02:08:11 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 07 Apr 2026 02:08:11 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:08:11 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 07 Apr 2026 02:08:11 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 02:08:12 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 07 Apr 2026 02:08:12 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 07 Apr 2026 02:08:13 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 07 Apr 2026 02:08:13 GMT
LABEL org.label-schema.build-date=2026-03-16T15:10:41.216Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2cc8a9176084bc48abad7a65cc3a3f5961c8d9cb org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.13 org.opencontainers.image.created=2026-03-16T15:10:41.216Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2cc8a9176084bc48abad7a65cc3a3f5961c8d9cb org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.13
# Tue, 07 Apr 2026 02:08:13 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 07 Apr 2026 02:08:13 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 07 Apr 2026 02:08:13 GMT
USER 1000
```

-	Layers:
	-	`sha256:689b91d88a0f4086057ec826027b128902ecf2b516be510371c115bc55da19a6`  
		Last Modified: Fri, 03 Apr 2026 15:56:29 GMT  
		Size: 29.7 MB (29733459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70746192819b381a2399233a8dc131b2cc80e1abe58d84cdcfff11c78d418d6`  
		Last Modified: Tue, 07 Apr 2026 02:09:14 GMT  
		Size: 9.4 MB (9434590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428b1453225967adcd366f4f8737348e8a8c7091185f966a16e7bfa7b90d6105`  
		Last Modified: Tue, 07 Apr 2026 02:09:23 GMT  
		Size: 407.4 MB (407415934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f07b601488c61c9f9dfdb53cb28a80724507237738daabe0830110687eb00a1`  
		Last Modified: Tue, 07 Apr 2026 02:09:14 GMT  
		Size: 9.5 KB (9528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c274d21a1698c7a8d64f6741effd175e0427764a09501751700e7eaf16fc29`  
		Last Modified: Tue, 07 Apr 2026 02:09:15 GMT  
		Size: 16.5 MB (16460487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4090c6cfb15dacd847690f69774889fe949359c42a1f73d6d4f784a40dbfa027`  
		Last Modified: Tue, 07 Apr 2026 02:09:15 GMT  
		Size: 5.2 KB (5237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41fa262846d317f6aea4ee0e4834d51206fa2bb9b663b2d3db39bb90cafee0b`  
		Last Modified: Tue, 07 Apr 2026 02:09:16 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2057d48f52445dc534e955d4b762fcf741d9f9c83278ae2af1be8a0da144225b`  
		Last Modified: Tue, 07 Apr 2026 02:09:16 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca465c2ad2344ea00fdb4e06046747916c1be13e47d54169ced574ff94b4f8b7`  
		Last Modified: Tue, 07 Apr 2026 02:09:17 GMT  
		Size: 4.8 KB (4815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb230778cce38ca2cd9cec1fc077496df2ce64a8c61f5cfae19296e29a39f70b`  
		Last Modified: Tue, 07 Apr 2026 02:09:17 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6806d84b32e3a51ae981a5acb1204f2a3590c0fe3828584c080304273ae3ee23`  
		Last Modified: Tue, 07 Apr 2026 02:09:18 GMT  
		Size: 161.7 KB (161740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e8f3be325d322a0d11fc853847bd0474fa12cba8264a4d9fa77b9e50136a03`  
		Last Modified: Tue, 07 Apr 2026 02:09:18 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.13` - unknown; unknown

```console
$ docker pull kibana@sha256:e008e40633572cedcb3da76e05bd4b0e198fa9453157eea22cd16cec7827d065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5041770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33fd87c5a9d6c4af030d3d8f523092d3a4e147bfffdc495687225cfebbb9ca19`

```dockerfile
```

-	Layers:
	-	`sha256:da365e0b753ac9d9ee02b7725278683908c0d5ab80c49a540ed84d024a5ec954`  
		Last Modified: Tue, 07 Apr 2026 02:09:14 GMT  
		Size: 5.0 MB (5000855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa88440017139fc14d6b95eaf173bffd24601e881228799d4ec7c669d7590550`  
		Last Modified: Tue, 07 Apr 2026 02:09:14 GMT  
		Size: 40.9 KB (40915 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:8.19.13` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:dd350900b3252ad9375608531cc49fcf750b4988c117d1dd35373af00e87930f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **476.1 MB (476117035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8885fd7dd7666c8da7fce1a17a1b44c98c0106eb08921e961dbe20a9b8f7700`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Fri, 03 Apr 2026 15:15:14 GMT
ARG RELEASE
# Fri, 03 Apr 2026 15:15:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 03 Apr 2026 15:15:14 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 03 Apr 2026 15:15:17 GMT
ADD file:9bab986009eae65b5534b3547eb3a7d0a1564404426de350dfd183cf3a4ffa9f in / 
# Fri, 03 Apr 2026 15:15:17 GMT
CMD ["/bin/bash"]
# Tue, 07 Apr 2026 02:02:18 GMT
EXPOSE map[5601/tcp:{}]
# Tue, 07 Apr 2026 02:02:18 GMT
RUN export DEBIAN_FRONTEND=noninteractive &&       apt-get update &&       apt-get install -y --no-install-recommends fontconfig fonts-liberation libnss3 curl ca-certificates &&       apt-get clean &&       rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:09:50 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Tue, 07 Apr 2026 02:09:51 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Tue, 07 Apr 2026 02:09:51 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Tue, 07 Apr 2026 02:09:51 GMT
RUN fc-cache -v # buildkit
# Tue, 07 Apr 2026 02:09:51 GMT
WORKDIR /usr/share/kibana
# Tue, 07 Apr 2026 02:09:51 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Tue, 07 Apr 2026 02:09:51 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 07 Apr 2026 02:09:51 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:09:51 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Tue, 07 Apr 2026 02:09:51 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Tue, 07 Apr 2026 02:09:52 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Tue, 07 Apr 2026 02:09:53 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Tue, 07 Apr 2026 02:09:53 GMT
RUN userdel -r ubuntu && groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Tue, 07 Apr 2026 02:09:53 GMT
LABEL org.label-schema.build-date=2026-03-16T15:10:41.216Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=2cc8a9176084bc48abad7a65cc3a3f5961c8d9cb org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=8.19.13 org.opencontainers.image.created=2026-03-16T15:10:41.216Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=2cc8a9176084bc48abad7a65cc3a3f5961c8d9cb org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=8.19.13
# Tue, 07 Apr 2026 02:09:53 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Tue, 07 Apr 2026 02:09:53 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Tue, 07 Apr 2026 02:09:53 GMT
USER 1000
```

-	Layers:
	-	`sha256:76fd055477b6edf8004a5a962edad02a820d4c8b2f02682410edfbe376b418c5`  
		Last Modified: Fri, 03 Apr 2026 15:56:36 GMT  
		Size: 28.9 MB (28874075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714820bfdef610fb9fa8aabf22c9dd3d81857b0d9faa1ed6d75d633cda6a1250`  
		Last Modified: Tue, 07 Apr 2026 02:11:06 GMT  
		Size: 9.5 MB (9452075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8dba8dc3f959889fb5f93917187537b081260249731dbcd58eb30ec373956ad`  
		Last Modified: Tue, 07 Apr 2026 02:11:14 GMT  
		Size: 421.2 MB (421150798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7db63902be1e0eecb0621868db9a545b1148335f5b48c86a2a839446a1764e`  
		Last Modified: Tue, 07 Apr 2026 02:11:05 GMT  
		Size: 9.1 KB (9096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68e6ffeeddf4e06de5e43debf84213edf5c2e46db5cb91362a81ee053e33430`  
		Last Modified: Tue, 07 Apr 2026 02:11:06 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa59ecceeb2b13aa629b4a0f87a6cdeae2de592139630302d01e65a799871669`  
		Last Modified: Tue, 07 Apr 2026 02:11:06 GMT  
		Size: 5.2 KB (5239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d426cf9975abc2e0bb3209ce4ce4a68390f5bfc7d37aaae5753f7c9c1402a076`  
		Last Modified: Tue, 07 Apr 2026 02:11:08 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7620dbca716946e99655455284bcfa16452553d93579156af6730a2548e7aef4`  
		Last Modified: Tue, 07 Apr 2026 02:11:07 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48dede2146106fa7a9036a4c749bd5b14daf51923f600497a67c28c9c180957f`  
		Last Modified: Tue, 07 Apr 2026 02:11:08 GMT  
		Size: 4.8 KB (4819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a76c44b8cf0b2c821aa61a876992fdb9623b1793e6003b2a10dccdcd26e646e`  
		Last Modified: Tue, 07 Apr 2026 02:11:09 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec9b07c7fbeb068c6990f22be41c4317ae4d335738b9a02dc088fdde7083aaa`  
		Last Modified: Tue, 07 Apr 2026 02:11:09 GMT  
		Size: 158.3 KB (158260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb8f2ec5eea24b26b0c15b5ae642c9afeed1834fd717db0413b787b2f502cf5`  
		Last Modified: Tue, 07 Apr 2026 02:11:09 GMT  
		Size: 1.2 KB (1225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:8.19.13` - unknown; unknown

```console
$ docker pull kibana@sha256:9c26e075eb9722fafabdd633b09b229bcb3a47e3c3519b7479804b8a9fb40618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5043082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e05fa321fe8e859a38b3aecebd722fe73e57c878a83d654e45f99a38d1b8762d`

```dockerfile
```

-	Layers:
	-	`sha256:b2aef8e28d9a32430d25ee471b299ebe135c50b45b0e04a27c8f69e4bb6b7f86`  
		Last Modified: Tue, 07 Apr 2026 02:11:05 GMT  
		Size: 5.0 MB (5001919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cd682dcba73dcf06fed315893cf25c46ff4c6f2e96a048a4314ec82dfd436c6`  
		Last Modified: Tue, 07 Apr 2026 02:11:05 GMT  
		Size: 41.2 KB (41163 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.2.7`

```console
$ docker pull kibana@sha256:8f335046a2c76b9bc7c1bdcce764cf787f360dd86720b86e0a7e324af749e822
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.2.7` - linux; amd64

```console
$ docker pull kibana@sha256:7e8ef13034eb0a6657c9db0ac0aa3f865670efddeaca9be9a9c7019f0f59811f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.1 MB (448066863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72227a349a3f09a0a92e3d5cd92d325717ea14b9f52fd03aeba29ebc10287f84`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 19 Mar 2026 17:02:51 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 17:02:51 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 19 Mar 2026 17:02:52 GMT
ENV container oci
# Thu, 19 Mar 2026 17:02:52 GMT
COPY dir:2cb6e43856cb0ad61489a8c64de98c252b875727203d4889684da9c688115b96 in /      
# Thu, 19 Mar 2026 17:02:52 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 17:02:52 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 17:02:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:289d553fe837e625c2f8fb767ab91c5be2d390395d3693929ca213958efa8fc8 in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:289d553fe837e625c2f8fb767ab91c5be2d390395d3693929ca213958efa8fc8 in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:02:53 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "org.opencontainers.image.revision"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "build-date"="2026-03-19T17:02:39Z" "org.opencontainers.image.created"="2026-03-19T17:02:39Z" "release"="1773939694"org.opencontainers.image.revision=d0c250a501ab44b94ebea3e751fcaa45749a08a2,org.opencontainers.image.created=2026-03-19T17:02:39Z
# Fri, 20 Mar 2026 00:18:02 GMT
EXPOSE map[5601/tcp:{}]
# Fri, 20 Mar 2026 00:18:02 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:27:09 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Fri, 20 Mar 2026 00:27:09 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Fri, 20 Mar 2026 00:27:09 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Fri, 20 Mar 2026 00:27:09 GMT
RUN fc-cache -v # buildkit
# Fri, 20 Mar 2026 00:27:09 GMT
WORKDIR /usr/share/kibana
# Fri, 20 Mar 2026 00:27:10 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Fri, 20 Mar 2026 00:27:10 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 20 Mar 2026 00:27:10 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:27:10 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Fri, 20 Mar 2026 00:27:10 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 00:27:10 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Fri, 20 Mar 2026 00:27:11 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Fri, 20 Mar 2026 00:27:11 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Fri, 20 Mar 2026 00:27:11 GMT
LABEL org.label-schema.build-date=2026-03-16T15:12:11.414Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=6bff11df59c8077810f373e3f4e2f2499ec906a9 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.7 org.opencontainers.image.created=2026-03-16T15:12:11.414Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=6bff11df59c8077810f373e3f4e2f2499ec906a9 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.7
# Fri, 20 Mar 2026 00:27:11 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.7 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Fri, 20 Mar 2026 00:27:11 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Fri, 20 Mar 2026 00:27:11 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Fri, 20 Mar 2026 00:27:11 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Fri, 20 Mar 2026 00:27:11 GMT
USER 1000
```

-	Layers:
	-	`sha256:75bed6ef625ff772ca48f63f12693f16f2b44649aa07030a7c4bc6b85225d5dd`  
		Last Modified: Thu, 19 Mar 2026 17:57:56 GMT  
		Size: 40.0 MB (40031119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158c00f0d00f642b9b918dd051fd5333de70de2b1033e80d796e35bf8adfb535`  
		Last Modified: Fri, 20 Mar 2026 00:28:07 GMT  
		Size: 19.5 MB (19527066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315fd8420c62c3eae8cec78c3b272dfd3ad5a2307b36eeabdbe1c75443b338e7`  
		Last Modified: Fri, 20 Mar 2026 00:28:14 GMT  
		Size: 372.0 MB (371950304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a74f65074184702c920d05f770dbf674d043a09c2eac2b75e593877defd0711`  
		Last Modified: Fri, 20 Mar 2026 00:28:06 GMT  
		Size: 9.5 KB (9531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c191ea46d9f7fb08f7602ed375f39f1e6f30658aad439d71361464fdffc89e7`  
		Last Modified: Fri, 20 Mar 2026 00:28:07 GMT  
		Size: 16.5 MB (16460475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f5b51270bf7659a1db6efade2eefadced104eb253c2ef7d33483dae0d7af89`  
		Last Modified: Fri, 20 Mar 2026 00:28:07 GMT  
		Size: 5.2 KB (5225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e0b4e5a6e3c2af50e2ac4efae50d2b8564ff58021e65e13d2390ed5dbf453c`  
		Last Modified: Fri, 20 Mar 2026 00:28:09 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5f99613c61b0eaada5fe265472488ff3aa1c929f33a8e7820e141858516f73`  
		Last Modified: Fri, 20 Mar 2026 00:28:09 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f3483c8581ed2da90692c2b18dfe426a8ec6fd583f1c1e5a6e3435d1112458`  
		Last Modified: Fri, 20 Mar 2026 00:28:09 GMT  
		Size: 4.9 KB (4895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee715e9f81d46946015ce163304250a283233b0b73e5c5662e34d738353553e`  
		Last Modified: Fri, 20 Mar 2026 00:28:10 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ec46933e6632833d6e1d3442b270fb46472a6cb34cc23b7138b3f1bf7ba948`  
		Last Modified: Fri, 20 Mar 2026 00:28:10 GMT  
		Size: 74.5 KB (74540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d5f4a4e4e3a527595f83a7b6e63a9668e680a067f445ef061ea9b8655111c3`  
		Last Modified: Fri, 20 Mar 2026 00:28:11 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:588cf650b981cfc5fabfb5a7129a2ed704217d7bd80b62a251d8517141b803a7`  
		Last Modified: Fri, 20 Mar 2026 00:28:11 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.7` - unknown; unknown

```console
$ docker pull kibana@sha256:b779d3e982bd5df6cdce4ed1545d881ac1503a7f9301b6b8f3010299d90e3d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5782390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef574fb46ed3c688df4645946cf923b733893f6b0812782fd33fbb283bc5f4b3`

```dockerfile
```

-	Layers:
	-	`sha256:d691f4c3bffa2ef3d56d5555a0a2be824b0f50ad25aa66e09a0d8d9df6f6ab7e`  
		Last Modified: Fri, 20 Mar 2026 00:28:07 GMT  
		Size: 5.7 MB (5739164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dccf7f33ea0b8bcfab49d8ed33d3ce2ba0d790c11c3b7aabacb4d732bab0a103`  
		Last Modified: Fri, 20 Mar 2026 00:28:06 GMT  
		Size: 43.2 KB (43226 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.2.7` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:867d36a7d00a4774e1f33d7ac41ab1c8e96a9415868419769dd72f7e4d733416
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.9 MB (459900146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8348ffcc407df9cdb57f75f4d5b0b7bf2abef2922523dc1ee4555371b30b69d2`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 19 Mar 2026 17:04:53 GMT
ENV container oci
# Thu, 19 Mar 2026 17:04:54 GMT
COPY dir:ebed5b428b4d7b7bd491e92b7639c4e00e22e8a9993f0cbde996cf63a3263224 in /      
# Thu, 19 Mar 2026 17:04:54 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 17:04:54 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:819fd782db190e306ad6dedf6720029cee5c6639348ef8be1d7fa1456c09e46b in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:819fd782db190e306ad6dedf6720029cee5c6639348ef8be1d7fa1456c09e46b in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:04:55 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "org.opencontainers.image.revision"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "build-date"="2026-03-19T17:04:41Z" "org.opencontainers.image.created"="2026-03-19T17:04:41Z" "release"="1773939694"org.opencontainers.image.revision=d0c250a501ab44b94ebea3e751fcaa45749a08a2,org.opencontainers.image.created=2026-03-19T17:04:41Z
# Fri, 20 Mar 2026 00:15:40 GMT
EXPOSE map[5601/tcp:{}]
# Fri, 20 Mar 2026 00:15:40 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:23:16 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Fri, 20 Mar 2026 00:23:17 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Fri, 20 Mar 2026 00:23:17 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Fri, 20 Mar 2026 00:23:17 GMT
RUN fc-cache -v # buildkit
# Fri, 20 Mar 2026 00:23:17 GMT
WORKDIR /usr/share/kibana
# Fri, 20 Mar 2026 00:23:17 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Fri, 20 Mar 2026 00:23:17 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 20 Mar 2026 00:23:17 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:23:17 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Fri, 20 Mar 2026 00:23:17 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 00:23:18 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Fri, 20 Mar 2026 00:23:19 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Fri, 20 Mar 2026 00:23:20 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Fri, 20 Mar 2026 00:23:20 GMT
LABEL org.label-schema.build-date=2026-03-16T15:12:11.414Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=6bff11df59c8077810f373e3f4e2f2499ec906a9 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.2.7 org.opencontainers.image.created=2026-03-16T15:12:11.414Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=6bff11df59c8077810f373e3f4e2f2499ec906a9 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.2.7
# Fri, 20 Mar 2026 00:23:20 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.2.7 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Fri, 20 Mar 2026 00:23:20 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Fri, 20 Mar 2026 00:23:20 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Fri, 20 Mar 2026 00:23:20 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Fri, 20 Mar 2026 00:23:20 GMT
USER 1000
```

-	Layers:
	-	`sha256:58b15a07209fe35d94749ac0349d53a753811f2289c2cd68bbdf7aefa4462360`  
		Last Modified: Thu, 19 Mar 2026 18:10:21 GMT  
		Size: 38.2 MB (38204902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9275199e0bc32bfbaf2f60882f9de4074acbf7bcfbbcaf54addc8354734b4c`  
		Last Modified: Fri, 20 Mar 2026 00:24:24 GMT  
		Size: 19.5 MB (19482613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458e65221886f009d2871d76c35fe52a317e36ef0fedc660d43ecb4e2044e833`  
		Last Modified: Fri, 20 Mar 2026 00:24:38 GMT  
		Size: 385.7 MB (385655762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a488a9d464afcd296c7393e80dd9a23b03d22f73ae807491294c60ef3078ac3`  
		Last Modified: Fri, 20 Mar 2026 00:24:23 GMT  
		Size: 9.1 KB (9098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a986c9038aa35c70c05ac2016697f1b003ffa09f2aab91961ff51f8fedc47a9`  
		Last Modified: Fri, 20 Mar 2026 00:24:24 GMT  
		Size: 16.5 MB (16460492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93d88175ed205800d520bf3d1cf627c601d67cdebca70933c23be06e95e2c78`  
		Last Modified: Fri, 20 Mar 2026 00:24:24 GMT  
		Size: 5.2 KB (5222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096ad794a5b744de656d79d41c9a6f338530c344694b4e49e2de1e80e6a567e9`  
		Last Modified: Fri, 20 Mar 2026 00:24:26 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1395f7048a7b64353cc1dfebb9601542b570d16f488c68baff58606b0ac563bf`  
		Last Modified: Fri, 20 Mar 2026 00:24:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c50133b34d04701bd1cc21c0a5e1cb0d98007af81e251368b296edf1adb273`  
		Last Modified: Fri, 20 Mar 2026 00:24:26 GMT  
		Size: 4.9 KB (4896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574208916abf910cf44cdcef5077d8f75683bf5d06839923ac698ea4dc9dc87f`  
		Last Modified: Fri, 20 Mar 2026 00:24:27 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb573d852f8fb9587bf1fccf23c0d824af286abe4c444aeeea118bcc4d1ed1a`  
		Last Modified: Fri, 20 Mar 2026 00:24:27 GMT  
		Size: 73.5 KB (73450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa154abcd1a245a155230f506d2b364ad044733e8973fd850a7ff7efc8436e0e`  
		Last Modified: Fri, 20 Mar 2026 00:24:27 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2152eacffb07dd6f6acea5abc076c8b759e8478b2ee2bf1245f2f8e99831a96`  
		Last Modified: Fri, 20 Mar 2026 00:24:28 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.2.7` - unknown; unknown

```console
$ docker pull kibana@sha256:31d99df790721369f78081f90510d88fa2743815a0d9db467d7a1a8bc370a433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5781319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75eab03e50116c954a980060cd5ca0bd7c439f9f7cc184665c10b4b508cb34bf`

```dockerfile
```

-	Layers:
	-	`sha256:89079c28113a6f0120f7e101b1aac6e6fcab005560a23fef5730f070d5dd636f`  
		Last Modified: Fri, 20 Mar 2026 00:24:23 GMT  
		Size: 5.7 MB (5737836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c079bb1501a1ca51c14c249d2facd708cc9b639e7c8d2c6739ada0b8cb153c9f`  
		Last Modified: Fri, 20 Mar 2026 00:24:22 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json

## `kibana:9.3.2`

```console
$ docker pull kibana@sha256:7886fd29da6bd592f203946f58de1eb3937d19811008b920d46380078661a4f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kibana:9.3.2` - linux; amd64

```console
$ docker pull kibana@sha256:f3bad537b2851f8f042771d51874ab1d153f9224866aa7dca648ba5e7d4fdd19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **453.5 MB (453472992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:545df989a40906c7a06f79198be6f4909afa9745b14f67fcf3eb084d59b56e20`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 19 Mar 2026 17:02:51 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 17:02:51 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 17:02:52 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 19 Mar 2026 17:02:52 GMT
ENV container oci
# Thu, 19 Mar 2026 17:02:52 GMT
COPY dir:2cb6e43856cb0ad61489a8c64de98c252b875727203d4889684da9c688115b96 in /      
# Thu, 19 Mar 2026 17:02:52 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 17:02:52 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 17:02:52 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:289d553fe837e625c2f8fb767ab91c5be2d390395d3693929ca213958efa8fc8 in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:02:53 GMT
COPY file:289d553fe837e625c2f8fb767ab91c5be2d390395d3693929ca213958efa8fc8 in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:02:53 GMT
LABEL "architecture"="x86_64" "vcs-type"="git" "vcs-ref"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "org.opencontainers.image.revision"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "build-date"="2026-03-19T17:02:39Z" "org.opencontainers.image.created"="2026-03-19T17:02:39Z" "release"="1773939694"org.opencontainers.image.revision=d0c250a501ab44b94ebea3e751fcaa45749a08a2,org.opencontainers.image.created=2026-03-19T17:02:39Z
# Fri, 20 Mar 2026 00:18:06 GMT
EXPOSE map[5601/tcp:{}]
# Fri, 20 Mar 2026 00:18:06 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:27:47 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Fri, 20 Mar 2026 00:27:47 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Fri, 20 Mar 2026 00:27:47 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Fri, 20 Mar 2026 00:27:47 GMT
RUN fc-cache -v # buildkit
# Fri, 20 Mar 2026 00:27:47 GMT
WORKDIR /usr/share/kibana
# Fri, 20 Mar 2026 00:27:48 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Fri, 20 Mar 2026 00:27:48 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 20 Mar 2026 00:27:48 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:27:48 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Fri, 20 Mar 2026 00:27:48 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 00:27:48 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Fri, 20 Mar 2026 00:27:49 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Fri, 20 Mar 2026 00:27:49 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Fri, 20 Mar 2026 00:27:49 GMT
LABEL org.label-schema.build-date=2026-03-16T15:02:29.765Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=80a75d1ae44e8a67f79adf9709bba3075d85afc7 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.2 org.opencontainers.image.created=2026-03-16T15:02:29.765Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=80a75d1ae44e8a67f79adf9709bba3075d85afc7 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.2
# Fri, 20 Mar 2026 00:27:49 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.2 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Fri, 20 Mar 2026 00:27:49 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Fri, 20 Mar 2026 00:27:49 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Fri, 20 Mar 2026 00:27:49 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Fri, 20 Mar 2026 00:27:49 GMT
USER 1000
```

-	Layers:
	-	`sha256:75bed6ef625ff772ca48f63f12693f16f2b44649aa07030a7c4bc6b85225d5dd`  
		Last Modified: Thu, 19 Mar 2026 17:57:56 GMT  
		Size: 40.0 MB (40031119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89496a316b8f7e701706bfaf0eae07c68edb7592de92c6924c0ace3c1e4dfde`  
		Last Modified: Fri, 20 Mar 2026 00:28:48 GMT  
		Size: 19.5 MB (19527080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6858569cf7b8749667af954885f1462e73f247be5fb92e6d58dbe51b258f28`  
		Last Modified: Fri, 20 Mar 2026 00:28:55 GMT  
		Size: 377.4 MB (377356380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8e3a02a7f7838ead497b184ee9da608427351832d01ca5233eaa449fdab311`  
		Last Modified: Fri, 20 Mar 2026 00:28:47 GMT  
		Size: 9.5 KB (9532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42706a01a7101bf221ae9fd82d5a201aea9eea2b03e0b08964d3050763afeffa`  
		Last Modified: Fri, 20 Mar 2026 00:28:48 GMT  
		Size: 16.5 MB (16460488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f2b72db7b76322f6cf314a0dc44293530e7430ac1523f0aeedf99c1087a105`  
		Last Modified: Fri, 20 Mar 2026 00:28:48 GMT  
		Size: 5.2 KB (5226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336490822199c9edef27264f7fbb6cc58a27a4bf74561f53ab12798ef23a573b`  
		Last Modified: Fri, 20 Mar 2026 00:28:50 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e290f6c1b3aa62a9463f4d64ce60c8581233912680333891375e0069a319b5c0`  
		Last Modified: Fri, 20 Mar 2026 00:28:50 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66eb6224473a1f4166223891fec72e7127b9e2be829b58702528dc19d346d6bf`  
		Last Modified: Fri, 20 Mar 2026 00:28:50 GMT  
		Size: 4.9 KB (4916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558e3cd9c4c0e7e8a48be204c7c0ef78d921b0a78c3e3be39d210872eeb2cc4a`  
		Last Modified: Fri, 20 Mar 2026 00:28:51 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3121e5fb681ce41103b9498d68691f3337bb3569dc6e7d87bf79175b1fdacbd9`  
		Last Modified: Fri, 20 Mar 2026 00:28:51 GMT  
		Size: 74.5 KB (74541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4261ff71c87157c9d5392c2ec477308b59cf37452854cc3611990f9fa655160e`  
		Last Modified: Fri, 20 Mar 2026 00:28:51 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9134951689b959482420cafc6c5a4d0edf36bc469a23bc18a2db06b255cdc0f`  
		Last Modified: Fri, 20 Mar 2026 00:28:52 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.2` - unknown; unknown

```console
$ docker pull kibana@sha256:51a7762562ee1ea2e61797147fb211f82613d10cbbe3b06398aef09f8b6ac198
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5849281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16670133a56901954893a4ba1ce4ce9049b309c6e725c96103a453f90b0e2e1`

```dockerfile
```

-	Layers:
	-	`sha256:6b24190c07ad63fa65fca12d7cd52ed57d2a76895df65d9d5c97667559966583`  
		Last Modified: Fri, 20 Mar 2026 00:28:47 GMT  
		Size: 5.8 MB (5806057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dfa09454a752e3c9bd679fd337861593f42ff8ddd5cbf5b902407af018210a7c`  
		Last Modified: Fri, 20 Mar 2026 00:28:47 GMT  
		Size: 43.2 KB (43224 bytes)  
		MIME: application/vnd.in-toto+json

### `kibana:9.3.2` - linux; arm64 variant v8

```console
$ docker pull kibana@sha256:34613bac2a155cea44285c2e6a35a2e92f81be33c6b529b875b1b251da58fd20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **465.3 MB (465343872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a7750a0e4b859877354b6a85b0944e694ddc3968f0887c53c66b98aefc20c2`
-	Entrypoint: `["\/bin\/tini","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL maintainer="Red Hat, Inc."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL vendor="Red Hat, Inc."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL url="https://catalog.redhat.com/en/search?searchType=containers"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL com.redhat.component="ubi9-minimal-container"       name="ubi9/ubi-minimal"       version="9.7"       cpe="cpe:/a:redhat:enterprise_linux:9::appstream"       distribution-scope="public"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL com.redhat.license_terms="https://www.redhat.com/en/about/red-hat-end-user-license-agreements#UBI"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL summary="Provides the latest release of the minimal Red Hat Universal Base Image 9."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.k8s.description="The Universal Base Image Minimal is a stripped down image that uses microdnf as a package manager. This base image is freely redistributable, but Red Hat only supports Red Hat technologies through subscriptions for Red Hat products. This image is maintained by Red Hat and updated regularly."
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.k8s.display-name="Red Hat Universal Base Image 9 Minimal"
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.openshift.expose-services=""
# Thu, 19 Mar 2026 17:04:53 GMT
LABEL io.openshift.tags="minimal rhel9"
# Thu, 19 Mar 2026 17:04:53 GMT
ENV container oci
# Thu, 19 Mar 2026 17:04:54 GMT
COPY dir:ebed5b428b4d7b7bd491e92b7639c4e00e22e8a9993f0cbde996cf63a3263224 in /      
# Thu, 19 Mar 2026 17:04:54 GMT
COPY file:1376702515d596f414e3aa494e0daa6d408a6d2475c4aeca96bf9392f5287f69 in /etc/yum.repos.d/.      
# Thu, 19 Mar 2026 17:04:54 GMT
CMD ["/bin/bash"]
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /usr/share/buildinfo/content-sets.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:93583a9ebbaeff1e36b48820b647eea1eef523f6627dacfb0b21af79f5a41b35 in /root/buildinfo/content_manifests/content-sets.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:819fd782db190e306ad6dedf6720029cee5c6639348ef8be1d7fa1456c09e46b in /usr/share/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:04:55 GMT
COPY file:819fd782db190e306ad6dedf6720029cee5c6639348ef8be1d7fa1456c09e46b in /root/buildinfo/labels.json      
# Thu, 19 Mar 2026 17:04:55 GMT
LABEL "architecture"="aarch64" "vcs-type"="git" "vcs-ref"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "org.opencontainers.image.revision"="d0c250a501ab44b94ebea3e751fcaa45749a08a2" "build-date"="2026-03-19T17:04:41Z" "org.opencontainers.image.created"="2026-03-19T17:04:41Z" "release"="1773939694"org.opencontainers.image.revision=d0c250a501ab44b94ebea3e751fcaa45749a08a2,org.opencontainers.image.created=2026-03-19T17:04:41Z
# Fri, 20 Mar 2026 00:16:06 GMT
EXPOSE map[5601/tcp:{}]
# Fri, 20 Mar 2026 00:16:06 GMT
RUN microdnf install --setopt=tsflags=nodocs -y       fontconfig liberation-fonts-common freetype shadow-utils nss findutils &&       microdnf clean all # buildkit
# Fri, 20 Mar 2026 00:23:53 GMT
COPY --chown=1000:0 /usr/share/kibana /usr/share/kibana # buildkit
# Fri, 20 Mar 2026 00:23:53 GMT
COPY --chown=0:0 /bin/tini /bin/tini # buildkit
# Fri, 20 Mar 2026 00:23:53 GMT
COPY --chown=0:0 /usr/share/fonts/local/NotoSansCJK-Regular.ttc /usr/share/fonts/local/NotoSansCJK-Regular.ttc # buildkit
# Fri, 20 Mar 2026 00:23:53 GMT
RUN fc-cache -v # buildkit
# Fri, 20 Mar 2026 00:23:54 GMT
WORKDIR /usr/share/kibana
# Fri, 20 Mar 2026 00:23:54 GMT
RUN ln -s /usr/share/kibana /opt/kibana # buildkit
# Fri, 20 Mar 2026 00:23:54 GMT
ENV ELASTIC_CONTAINER=true
# Fri, 20 Mar 2026 00:23:54 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 20 Mar 2026 00:23:54 GMT
COPY --chown=1000:0 config/kibana.yml /usr/share/kibana/config/kibana.yml # buildkit
# Fri, 20 Mar 2026 00:23:54 GMT
COPY bin/kibana-docker /usr/local/bin/ # buildkit
# Fri, 20 Mar 2026 00:23:55 GMT
RUN chmod g+ws /usr/share/kibana &&     find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \; # buildkit
# Fri, 20 Mar 2026 00:23:56 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} + # buildkit
# Fri, 20 Mar 2026 00:23:56 GMT
RUN groupadd --gid 1000 kibana &&     useradd --uid 1000 --gid 1000 -G 0       --home-dir /usr/share/kibana --no-create-home       kibana # buildkit
# Fri, 20 Mar 2026 00:23:56 GMT
LABEL org.label-schema.build-date=2026-03-16T15:02:29.765Z org.label-schema.license=Elastic License org.label-schema.name=Kibana org.label-schema.schema-version=1.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.usage=https://www.elastic.co/guide/en/kibana/reference/index.html org.label-schema.vcs-ref=80a75d1ae44e8a67f79adf9709bba3075d85afc7 org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.vendor=Elastic org.label-schema.version=9.3.2 org.opencontainers.image.created=2026-03-16T15:02:29.765Z org.opencontainers.image.documentation=https://www.elastic.co/guide/en/kibana/reference/index.html org.opencontainers.image.licenses=Elastic License org.opencontainers.image.revision=80a75d1ae44e8a67f79adf9709bba3075d85afc7 org.opencontainers.image.source=https://github.com/elastic/kibana org.opencontainers.image.title=Kibana org.opencontainers.image.url=https://www.elastic.co/products/kibana org.opencontainers.image.vendor=Elastic org.opencontainers.image.version=9.3.2
# Fri, 20 Mar 2026 00:23:56 GMT
LABEL name=Kibana maintainer=infra@elastic.co vendor=Elastic version=9.3.2 release=1 summary=Kibana description=Your window into the Elastic Stack.
# Fri, 20 Mar 2026 00:23:56 GMT
RUN mkdir /licenses && ln LICENSE.txt /licenses/LICENSE # buildkit
# Fri, 20 Mar 2026 00:23:56 GMT
ENTRYPOINT ["/bin/tini" "--"]
# Fri, 20 Mar 2026 00:23:56 GMT
CMD ["/usr/local/bin/kibana-docker"]
# Fri, 20 Mar 2026 00:23:56 GMT
USER 1000
```

-	Layers:
	-	`sha256:58b15a07209fe35d94749ac0349d53a753811f2289c2cd68bbdf7aefa4462360`  
		Last Modified: Thu, 19 Mar 2026 18:10:21 GMT  
		Size: 38.2 MB (38204902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce340a5c93f21dfa9c76fe18b273103accb6fb7af03ab21816048d5c470dc00`  
		Last Modified: Fri, 20 Mar 2026 00:25:01 GMT  
		Size: 19.5 MB (19482481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b218c820d958e6dddd5c6ddcf32a9075146ac93469dad4b1886b2cbaea4696`  
		Last Modified: Fri, 20 Mar 2026 00:25:08 GMT  
		Size: 391.1 MB (391099609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec4be1f8ceeec4e3ed764b73dce315e53dc4bf2d8b1ab817ae42c70a8fde825`  
		Last Modified: Fri, 20 Mar 2026 00:25:00 GMT  
		Size: 9.1 KB (9099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844e66f6f56e27c51b7a8516d5dad7f88f53e267429e293eb2ac9345705f3146`  
		Last Modified: Fri, 20 Mar 2026 00:25:01 GMT  
		Size: 16.5 MB (16460492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33cf014f5898b9112c6e6c866cddf4c06dfe75b6670bbf00fc290e96a0e1cae7`  
		Last Modified: Fri, 20 Mar 2026 00:25:01 GMT  
		Size: 5.2 KB (5223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7957c4eaf8d364b1f284f51eac616d80519ff01fc74b183fdacc6ba8aa4393d7`  
		Last Modified: Fri, 20 Mar 2026 00:25:03 GMT  
		Size: 130.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11200a25243470c745ee0604f2b42ead4a6683d4ecbeb162174e2f644d2450c2`  
		Last Modified: Fri, 20 Mar 2026 00:25:03 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfb9013cfb001e52801434491f958adf3558ae82f267e7e5e72d826d596151b`  
		Last Modified: Fri, 20 Mar 2026 00:25:03 GMT  
		Size: 4.9 KB (4912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9343f91a6fc111070c3a5a9f5c5488f1460ab7e296f0a4c838360882c5a0842`  
		Last Modified: Fri, 20 Mar 2026 00:25:04 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c0b8c99ae972c09805ca992284b639207fbeb0d24779bcfb8606281f6e1c89`  
		Last Modified: Fri, 20 Mar 2026 00:25:04 GMT  
		Size: 73.5 KB (73450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6090fdac0b9233f589287f0269cb466ff9e552ac64d9de7d7a135eede511db6c`  
		Last Modified: Fri, 20 Mar 2026 00:25:04 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbd02696084050fc0d20564d885d37fc32b529c2d082aaa5ec4af7497843081`  
		Last Modified: Fri, 20 Mar 2026 00:25:05 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kibana:9.3.2` - unknown; unknown

```console
$ docker pull kibana@sha256:9de9517f3891ee8f869f07997611466e4a77463e2680a9148c51afcbe2379cca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5848212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3edfa5e8ffa52f11dd382d327215e2ed0b8a4e8c44c8895cf222617c1c9c1a34`

```dockerfile
```

-	Layers:
	-	`sha256:7fa75ec42a6275658f862dbc683e1eab0bc8b4958063f125404acc731debdc71`  
		Last Modified: Fri, 20 Mar 2026 00:25:00 GMT  
		Size: 5.8 MB (5804729 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:703e43bb27462ef05d480a286b9a33c9780153ed5934aabaeab6dab701aaffc5`  
		Last Modified: Fri, 20 Mar 2026 00:25:00 GMT  
		Size: 43.5 KB (43483 bytes)  
		MIME: application/vnd.in-toto+json
