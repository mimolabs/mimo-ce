# MIMO Community Edition

The MIMO Community Edition is a feature rich guest WiFi system that you install on your own servers.

It includes everything you need to operate a guest network. This includes:

1. Splash pages
2. Email capture
3. Email campaigns (coming soon)

It works with Ubiquiti UniFi only right now but we'll be adding support for Ruckus, Cisco, Aruba, OpenMesh, Meraki and more soon.

### Integration MIMO

MIMO currently works with UniFi devices only. Your UniFi controller must have a public IP and be accessible. The CE integrations work in the same way as our enterprise version. The docs for this can be found [here](https://docs.oh-mimo.com/integrations/ubiquiti-unifi-splash-integration).

Connecting MIMO to your UniFi controller should take less than 30 seconds. The MIMO service will set everything up for you including a guest SSID, captive portal.

### The core modules include:

- API server for handling requests
- AngularJS dashboard for management of your splash pages etc
- Splash pages for guest access

### What's the difference between this and the hosted MIMO?

At the time of writing, MIMO CE is almost idential to the enterprise version with some caveats.

- It only supports UniFi access points (for now)
- It doesn't include a radius module (yet)
- It doesn't include live support

### Free Support

The standard MIMO docs are [here](https://docs.oh-mimo.com). These don't include much information about the Community Edition yet. 

The brand-new forum can be found [here](https://discuss.oh-mimo.com/).

We don't offer email or phone support - if you have a problem, please start a conversation on the forums.

### Enterprise Support

You can purchase enterprise support for the Community Edition - just email us on team@oh-mimo.com to discuss.

### Hosting

If you need us to host your MIMO service, you can sign-up for one of the enterprise plans over [here](https://oh-mimo.com/plans).

### Installation Support

We can install MIMO for you on your own Digital Ocean server for $149 USD. Please note: there's an ongoing cost of $10 per month for the server (MIMO needs at least 2Gb RAM). You pay the ongoing costs to Digital Ocean directly. 

Create your Digital Ocean server [here](https://m.do.co/c/8504487cbb3a) (this link gives you $10 credit so you get a month free). Then drop us a line on team@oh-mimo and we'll sort the rest. 

You must have your domain, DNS and email credentials ready. 

Please note, we don't offer post-installation support. You'll need to get on the forums or sing-up for enterprise support.

## Copyright / License

Copyright 2018 Cucumber Tony, trading as MIMO.

Licensed under the GNU General Public License Version 2.0 (or later);
you may not use this work except in compliance with the License.
You may obtain a copy of the License in the LICENSE file, or at:

   http://www.gnu.org/licenses/old-licenses/gpl-2.0.txt

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
