<template>
    <section class="body-container">
        <div class="body-navbar">
            <ul>
                <li>{{ $t('message.menu_phone') }}</li>
                <li>{{ $t('message.menu_book') }}</li>
                <li>{{ $t('message.menu_one_computer') }}</li>
                <li>{{ $t('message.menu_desktop_computer') }}</li>
                <li>{{ $t('message.menu_printer') }}</li>
                <li>{{ $t('message.menu_projector') }}</li>
            </ul>
        </div>
        <Carousel class="body-Carousel" autoplay loop>
            <CarouselItem>
                <div class="demo-carousel">1</div>
            </CarouselItem>
            <CarouselItem>
                <div class="demo-carousel">2</div>
            </CarouselItem>
            <CarouselItem>
                <div class="demo-carousel">3</div>
            </CarouselItem>
            <CarouselItem>
                <div class="demo-carousel">4</div>
            </CarouselItem>
        </Carousel>
        <section>
            <SectionHead :title="$t('message.component_preference')" :des="$t('message.component_preference_partner')"/>
            <Tabs value="name1">
                <TabPane :label="$t('message.component_scene_classification_However')" name="name1">
                    <CommodityListModel
                        :goodsList="goodsList"
                    />
                </TabPane>
                <TabPane :label="$t('message.component_scene_classification_pic')" name="name2">标签二的内容</TabPane>
                <TabPane :label="$t('message.component_scene_classification_com')" name="name3">标签三的内容</TabPane>
                <TabPane :label="$t('message.component_scene_classification_down')" name="name4">标签四的内容</TabPane>
            </Tabs>
        </section>
    </section>
</template>

<script>
import SectionHead from './components/SectionHead'
import CommodityListModel from '@/components/CommodityListModel'
export default {
    name: 'home',
    components: {
        SectionHead,
        CommodityListModel
    },
    data() {
        return {
            goodsList: [{
                picture: 'https://static2.zugeliang01.com/lease/img/fecd4f00-409a-11e9-b414-f1a0a794309d.png',
                goodsName: 'lalal',
                goodsDetail: 'oiuqioweqlqjlk',
                leaseMinPrice: 199.2,
                unit: 29,
                leaseMinPrice: 2131,
            },{
                picture: 'https://static2.zugeliang01.com/lease/img/fecd4f00-409a-11e9-b414-f1a0a794309d.png',
                goodsName: 'lalal',
                goodsDetail: 'oiuqioweqlqjlk',
                leaseMinPrice: '199.2',
                unit: '29',
                leaseMinPrice: '2131',
            },{
                picture: 'https://static2.zugeliang01.com/lease/img/fecd4f00-409a-11e9-b414-f1a0a794309d.png',
                goodsName: 'lalal',
                goodsDetail: 'oiuqioweqlqjlk',
                leaseMinPrice: '199.2',
                unit: '29',
                leaseMinPrice: '2131',
            },{
                picture: 'https://static2.zugeliang01.com/lease/img/fecd4f00-409a-11e9-b414-f1a0a794309d.png',
                goodsName: 'lalal',
                goodsDetail: 'oiuqioweqlqjlk',
                leaseMinPrice: '199.2',
                unit: '29',
                leaseMinPrice: '2131',
            },{
                picture: 'https://static2.zugeliang01.com/lease/img/fecd4f00-409a-11e9-b414-f1a0a794309d.png',
                goodsName: 'lalal',
                goodsDetail: 'oiuqioweqlqjlk',
                leaseMinPrice: '199.2',
                unit: '29',
                leaseMinPrice: '2131',
            },{
                picture: 'https://static2.zugeliang01.com/lease/img/fecd4f00-409a-11e9-b414-f1a0a794309d.png',
                goodsName: 'lalal',
                goodsDetail: 'oiuqioweqlqjlk',
                leaseMinPrice: '199.2',
                unit: '29',
                leaseMinPrice: '2131',
            },{
                picture: 'https://static2.zugeliang01.com/lease/img/fecd4f00-409a-11e9-b414-f1a0a794309d.png',
                goodsName: 'lalal',
                goodsDetail: 'oiuqioweqlqjlk',
                leaseMinPrice: '199.2',
                unit: '29',
                leaseMinPrice: '2131',
            },{
                picture: 'https://static2.zugeliang01.com/lease/img/fecd4f00-409a-11e9-b414-f1a0a794309d.png',
                goodsName: 'lalal',
                goodsDetail: 'oiuqioweqlqjlk',
                leaseMinPrice: '199.2',
                unit: '29',
                leaseMinPrice: '2131',
            }]
        }
    },
    methods: {
        handleToDetail() {
            console.log(1)
        }
    }
}
</script>

<style lang="less" scoped>
@import "../../assets/less/main";
.body-container{
    .body-navbar{
        .size(100%, 60px);
        .box-shadow();
        ul{
            .size(1200px, 100%);
            margin: 0 auto;
            display: flex;
            li{
                .size(auto, 100%);
                .center(flex);
                .fz(@fontSize12);
                color:@colorFont666;
                padding: 0 18px;
            }
        }
    }
    .body-Carousel{
        .size(100%, 400px)
    }
    section{
        padding: 80px 0;
        .center(flex);
        flex-direction: column;
    }
}
</style>
