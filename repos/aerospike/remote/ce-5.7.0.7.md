## `aerospike:ce-5.7.0.7`

```console
$ docker pull aerospike@sha256:9ba5ce758854f10165003bae119d7ce16ec908ac527446eda142178a3d8a2b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ce-5.7.0.7` - linux; amd64

```console
$ docker pull aerospike@sha256:b373a76dff9a30ba537db79947cee7f59b9bed41326bcc0f3cbdbfc023670eb3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.5 MB (81519702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21fbea3856d67dd62f289aaddf58b5c0278cbc3547d5eca6835cb10491ed137c`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:07:29 GMT
ENV AEROSPIKE_VERSION=5.7.0.7
# Tue, 12 Oct 2021 02:07:57 GMT
ENV AEROSPIKE_SHA256=9cb4afd5305e2192813ce4551f3943917c5b25d2a372d8f8cf2b4f55ae376034
# Tue, 12 Oct 2021 02:08:16 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libcurl4-openssl-dev    && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Tue, 12 Oct 2021 02:08:17 GMT
COPY file:1897c4aae07efbc61bf2d8c2c7b0dfb0990174e11cc787eac71d5adf767abaed in /etc/aerospike/aerospike.template.conf 
# Tue, 12 Oct 2021 02:08:17 GMT
COPY file:e1d47057fdb4c34c118f7ba5898161c386b475cba70907a4ae483866cf07335b in /entrypoint.sh 
# Tue, 12 Oct 2021 02:08:17 GMT
EXPOSE 3000 3001 3002
# Tue, 12 Oct 2021 02:08:17 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Tue, 12 Oct 2021 02:08:17 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f06eee45befe27e35a90ad1c2e832ef77a0d5cc37ee3a3dcc17641fa820673`  
		Last Modified: Tue, 12 Oct 2021 02:08:50 GMT  
		Size: 54.4 MB (54378168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7c1873e8f89665ff855059aecf7478ce68e00f7f054008ba90ab4e6bb5b6f2`  
		Last Modified: Tue, 12 Oct 2021 02:08:42 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56d71effb68359a52c1106d612d69cc1db3b8eabc7720f29a69cea141a2bc15`  
		Last Modified: Tue, 12 Oct 2021 02:08:42 GMT  
		Size: 883.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
