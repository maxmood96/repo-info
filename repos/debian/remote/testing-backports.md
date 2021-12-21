## `debian:testing-backports`

```console
$ docker pull debian@sha256:613755619dc7e2e7ad452c6bd93d5c7e62ca5d8797493e6e3723140a7f446dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:dfca9b85ab886bb246fa3f0b253cf3d832652c756ccd76f13e07ebd5f683b209
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55599008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3bdb30cea6ee6a78740e302e39b3f72b7853a96b6697c69b77fff5d11e8a69d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:24:51 GMT
ADD file:d302405af930cc11493038d472572e46ae1d7253df1c141916634ac984b48b88 in / 
# Tue, 21 Dec 2021 01:24:52 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:24:55 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:277c3ceb6ade1082faa3e2b17e1f8fc09ac549df797657b97f6f47253b55f4d0`  
		Last Modified: Tue, 21 Dec 2021 01:31:57 GMT  
		Size: 55.6 MB (55598781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a841ce30c4c9dd50a4f4eefaa16b535a6ca42378f670ad2be5b574aef6f55476`  
		Last Modified: Tue, 21 Dec 2021 01:32:06 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:e75195aacb7e8c206eebd467c27c95bb107c4c1d75ab01d91faa6fad4e44cd19
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53058869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770103d63070f029a68c0440a9c3f313b920e2e85eaf171a479a850746cb9f27`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:56:32 GMT
ADD file:75f3725fc71edf7a45e5898b6b19b5644aa66b243f51a4f2e0ba9ed774117744 in / 
# Tue, 21 Dec 2021 01:56:33 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:56:46 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:5a247649ffca9becc22b6b1b112cb8100dd44080fba2342951c336f93aa9eb85`  
		Last Modified: Tue, 21 Dec 2021 02:14:33 GMT  
		Size: 53.1 MB (53058642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5ea67f168eb4e98525f8dcc953399b1b5a69db3accecee6e1ec56e8916746b`  
		Last Modified: Tue, 21 Dec 2021 02:14:45 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:1a49f71edde638bfaf68d25655f351339af8dc9fea3d9bd1af47b46af4d08c78
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50699092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282011f53620acbdfeece1548f8a309d62599aced8e5c64a5405111d3ea2dff7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:06:10 GMT
ADD file:852d29e00f3be74c46433b090096356995db9697d73063b7871b3d8836dfc6df in / 
# Tue, 21 Dec 2021 02:06:11 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:06:24 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0a831c9172650283b4c426c4f1869fdd807a06bdd0dfc14ea3a104eb2a0016e2`  
		Last Modified: Tue, 21 Dec 2021 02:23:30 GMT  
		Size: 50.7 MB (50698868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6027f8e1b87b5d497885d3394ab8586f456dccb69038e2ddc60440d11403bd5c`  
		Last Modified: Tue, 21 Dec 2021 02:23:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:7b0c522a52d260273ecbc95709c9aabf426a473b6ac760b50396597562eada92
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54598060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66714187b6378f00c5ef0b61d7d12ee9fdca355438ca67839b0b6836eeac03ae`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:44:49 GMT
ADD file:436a7cbc9b247e837b1662f418559e588633a07d97fbe015b61da9481fb8a8f0 in / 
# Tue, 21 Dec 2021 01:44:50 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:44:56 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ca972f55dc0f92867c66012e7edaba4ddfecaf3952bbd20e050677fdbce9fb70`  
		Last Modified: Tue, 21 Dec 2021 01:53:28 GMT  
		Size: 54.6 MB (54597836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7762072f71dd07afc77f174def188806b78b9350da91f791cecc387df2faf847`  
		Last Modified: Tue, 21 Dec 2021 01:53:38 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:5e84598344c352393e60dfe19bfb11aa34dc71c6cbb0892d083458301256e1d5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56659089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9469660171b7468bcde6944d869bd63c99ac60ffea8baa7a854b33b0ca6659a4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:43:44 GMT
ADD file:fab1ec7b084bb10dbc74380fb1e54f057fbcf6f2adff18fbe85ddbe3c9384bd3 in / 
# Tue, 21 Dec 2021 01:43:45 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:43:51 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:bfd913943f9efe4f7d6ee24376f044314cf7778304a152b131dabcde41c0e0b6`  
		Last Modified: Tue, 21 Dec 2021 01:54:16 GMT  
		Size: 56.7 MB (56658865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0ce75a702349433ddc42fe91d82e55a6e79092ae971261fa8e1082507cbb2d6`  
		Last Modified: Tue, 21 Dec 2021 01:54:27 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:32fa0394e26889b15b90d32991f81567913e7e3badbf597246f391bb2e2b360b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54303091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a56b2562c39986479e950f6d3ac1f4b37ee0adb349f929de69dd35a90b8e49`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:13:08 GMT
ADD file:6985b096cadfd0d582309663a0437eb60028f9a5183d479ebc563e39b139a8a8 in / 
# Tue, 21 Dec 2021 02:13:09 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:13:16 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:dd286ebfa4ab697b2396d0e4f50d9e9c9b1fb899eab1cc6876b455a3e0e8cd0d`  
		Last Modified: Tue, 21 Dec 2021 02:24:29 GMT  
		Size: 54.3 MB (54302865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a5f3a4b6c794ea2f6f04e58d778333bdd61e13ccd30d9c5f01b5576e4544`  
		Last Modified: Tue, 21 Dec 2021 02:24:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:4ff28459b5960ff71541b281214accb5dd62f114a6299e2df42d1897cc27e61c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59992000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ce8bf85297bdef2846ad52b663c307d39a0e5bb134727298600b00edc76832a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:23:49 GMT
ADD file:42a91d93da4ddbf83627c69ff38d40590c8f8d299ec93dbedcf1faa79105a3af in / 
# Tue, 21 Dec 2021 02:23:54 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:24:08 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e172119311a8de31a50bf3e0fad45f9b68bf5edceb8397100d47c7833f2ac0fb`  
		Last Modified: Tue, 21 Dec 2021 02:33:13 GMT  
		Size: 60.0 MB (59991777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5f20d26f966e3ff512efcf92517ee5a7e414c5593929cf2619011f8be02898`  
		Last Modified: Tue, 21 Dec 2021 02:33:24 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:555162d68e9ed12d159e08bb5cbca8b220b94a0286c4c7a3041a15ac002afeaa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53888621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0edaa6b225b01c8d18401a2488e3a10a3888cd41ebc75a332789163f98ec0d58`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 01:44:29 GMT
ADD file:fab1fb88494aec56291007be8c0c54cc9bf3f56228b1e709a070150030986221 in / 
# Tue, 21 Dec 2021 01:44:31 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 01:44:38 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:38bb00702c0ff4b51b50541d1787108666c6714b6282d619229305becf8d14f8`  
		Last Modified: Tue, 21 Dec 2021 01:50:33 GMT  
		Size: 53.9 MB (53888397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad63e4bfa25834511b868c121824106819fe64cb67642a54b96b6f769081a83d`  
		Last Modified: Tue, 21 Dec 2021 01:50:41 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
