# React-App-Capstone-Project
Little Lemon Restaurant
import * as React from 'react';
import { NavigationContainer } from '@react-navigation/native';
import { createNativeStackNavigator } from '@react-navigation/native-stack';
import OnboardingScreen from './screens/Onboarding';

const Stack = createNativeStackNavigator();

function App() {
  return (
    <NavigationContainer>
      <Stack.Navigator>
        <Stack.Screen name="Onboarding" component={OnboardingScreen} />
      </Stack.Navigator>
    </NavigationContainer>
  );
}

export default function App;

if (state.isLoading) {
     // We haven't finished reading from AsyncStorage yet
     return <SplashScreen />;
    }
    
    return (
     <Stack.Navigator>
       {state.isOnboardingCompleted ? (
         // Onboarding completed, user is signed in
         <Stack.Screen name="Profile" component={ProfileScreen} />
       ) : (
         // User is NOT signed in
         <Stack.Screen name="Onboarding" component={OnboardingScreen} />
       )}
     </Stack.Navigator>
    );
